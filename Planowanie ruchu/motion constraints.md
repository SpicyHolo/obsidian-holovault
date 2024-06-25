Ograniczenia ruchu są brane pod uwagę podczas planowania ruchu robota ([[motion planning]]).

### [[2D motion constraints]]
### [[collision detection]]

### Inne ograniczenia ruchu
- [[robot workspace]]
- [[static stability]]
- [[dynamic stability]]

### Ograniczenia kinematyczne i kinodynamiczne
Ograniczenia dzielimy również ze względu na:
- kinematyczne (nieholonomiczne) 
- kinodynamiczne (na kinematykę, ale również na $v$ i $a$)
*W literaturze również pojawia się termin planowania trakejtorii, jest to pojęcie najbarzdziej ogólne i obejmuje ono oba powyższe przykłady, ale może również dotyczyć wyznaczenia sterowania $u(t)$*

### Ograniczenia kinematyczne
Wynikają ze struktury robota/agenta:
- rodzaj aktuatorów (liniowe / obrotowe)
- odległość pomiędzy przegubami
- maksymalne prędkości w przegubach
*Przykładem jest planowanie trajektorii robota manipulacyjnego (rozwiązywanie kinematyki prostej i odwrotnej, unikanie osobliwości i kolizji)*
### Ograniczenia kinodynamiczne
Dodatkowo obejmują:
- maksymalne przyspieszenia w przegubach
- ograniczenia na $M$, $F$

![[inevitable collision states.png]]
*Kolizje dla różnych prędkości ruchu (Inevitable Collision States)*

### Przykład: Robot differential-drive
Stan robota: $\mathbf{x} = [x, y, \theta]^T$, sterowanie: $\mathbf{u} = [u_l, u_r]^T$
$$
\begin{cases}
\dot{x} = \frac{r}{2}(u_l + u_r)\cdot\cos(\theta)\\
\dot{y} = \frac{r}{2}(u_l + u_r)\cdot\sin(\theta)\\\\
\dot{\theta} = \frac{r}{L}(u_l-u_r)
\end{cases}
$$
![[diff drive.png]]

Kinematyka prosta (obliczenie nowego stanu):
$$
\begin{cases}
x_t = x_{t-1} + \frac{r}{2}(u_l + u_r)\cdot\cos(\theta) \Delta t\\
y_t = y_{t-1} + \frac{r}{2}(u_l + u_r)\cdot\sin(\theta) \Delta t\\
\theta_t = \theta_{t-1} + \frac{r}{L}(u_l - u_r) \Delta t
\end{cases}
$$
Prędkość kół na podstawie wartości zadanych:
$$
\begin{cases}
\dot{u_l} = \frac{\dot{x} - \left(\frac{L}{2}\cdot\dot{\theta}\right)}{r} \\
\dot{u_r} = \frac{\dot{x} + \left(\frac{L}{2}\cdot\dot{\theta}\right)}{r} \\
\end{cases}
$$
### Kinematyka typu samochodowego
![[Pasted image 20240626013413.png]]

### Reeds-Shepp Car
![[Pasted image 20240626013424.png]]

### Dubins Car
![[Pasted image 20240626013436.png]]

### Modelowanie dynamiki
• Uwzględnienie masy i momentów bezwładności
• Uwzględnienie momentów i sił przykładanych do obiektów
• Uwzględnienie ograniczeń na momenty/siły i przyspieszenia, wynikające z zastosowanych napędów (modelowanie napędów)
• Uwzględnianie zjawisk nieliniowych, np. poślizgów, itd
Dla robotów ([[robot dynamics]])
$$
\tau = M(q)\ddot{q} + C(q, \dot{q})\dot{q} + G(q)
$$


