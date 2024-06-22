Szukanie funkcji Lapunova

### Przykład
$\dot{x} = -x$, $V(x) = x^2$

$$
\dot{V}(x) = -2x^2 < 0, \forall_{x \neq 0}
$$
$$
\dot{V}(x) = -2x^2 = -2V(x) \implies exponential \; V(x)
$$
### Przykład II
$\dot{x} = -x + x^3$, $V(x) = x^2$
$$
\dot{V}(x) = 2x\left(-x+x^3 \right) = -2x^2 + 2x^4 = 2x^2 (x^2 -1)
$$ czyli brak globalnej stabilności, ale ...
$$
\begin{cases}
= 0 \text{ for } x \in 0,1,-1 \\
> 0 \text { for } \lvert x \lvert > 1 \\
< 0 \text { for } \lvert x \lvert < 0 \;\land \; x \neq 0
\end{cases}
$$
![[Pasted image 20240618114849.png]]
Region atrakcji $\implies$ invariant set

## Dynamic Programming
#TODO ???

### Przykład III ([[physical pendulum]])
$$
ml^2 \ddot{\theta} + mgl \sin(\theta) = u
$$
$E^d = mgl$
$$
V(x) = \frac{1}{2}(E(x) - E^d(x))^2
$$
$$
\tilde{E} = E(x) - E^d(x) 
$$
Funkcja Lapunova
$$
V(x) = \frac{1}{2}\tilde{E}^2(x)
$$
$\dot{\tilde{E}} = \dot{E}(x)$
$$
\dot{E} = \frac{\partial E}{\partial x} \dot{x} =
\frac{\partial E}{\partial \theta} \dot{\theta} +
\frac{\partial E}{\partial \dot{\theta}} \ddot{\theta} = 
\dot{\theta}mgl \sin(\theta) + ml^2\dot{\theta}\ddot{\theta} = \dot{\theta}u
$$
Jak dobrać $u$, aby $\dot{E} \leq 0$

$u = -k\dot{\theta}\;\tilde{E}^2 \implies V(x) = -k \dot{\theta}^2 \; \tilde{E}$
*mamy stabilność wykładniczą*:
$$
\dot{V}(x) = -2\dot{\theta}^2 \; \frac{1}{2}\tilde{E}^2
$$
## Szukanie funkcji Lyapunova jako optymalizacja
##### Wejście
- równanie dyn.
- parametryczna rodzina funkcji Lapunova (trig-poly) {$1$, $\cos(\theta)$, $sin\theta$, $\dot{\theta}^n$, ...}
$$
V(x) = a_0\cdot 1 + a_1 \cdot \cos(\theta) + ... + a_{10}\cdot cos^2(\theta)\cdot \sin(\theta) + ...
$$
##### Wyjście
- współczynniki wielomianu $V(X)$
- certyfikat spełnienia war. Lapunowa 

$$
\min_x f(x), g(x \leq 0)
$$
$x$ - wektor zmiennych decyzyjnych
$g(x)$ - wektor ograniczeń
$f(x)$ - składowa f. kosztu

### Przykład
$\min_a \left[l(s, a) + J(f(s, a)) \right]$ - opt. dyskretna
$min_u \left[ u^TRu +r^Tu + r_0 \right]$ - opt. ciągła

##### bang-bang
![[Pasted image 20240618121430.png]]
$$
\min_u \left[ r^Tu + r_s \right]
$$
dla $\lvert u \lvert \leq 1$.
$$
\dot{x} = f_1(x) + f_2(x)u
$$
##### Klasa optymalizacji wypukłych
![[Pasted image 20240618121634.png]]
tzn. prosta łącząca dwa punkty leży nad prostą

$$
\text{wypukłość} \implies \text{optimumm lokalne} = \text{globalne}
$$

#control_theory 

