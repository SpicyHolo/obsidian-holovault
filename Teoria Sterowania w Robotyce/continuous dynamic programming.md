Rozwiązaniem na *problemy dyskretyzacji* jest wykorzystanie ciągłej reprezentacji układu dynamicznego.

## Podstawowe definicje
$$
\dot{x} = f_c(x, u)
$$
#### Suma kosztów
$$
L = \int^\infty_0 l_c\left(x(t), u(t)\right)dt
$$
#### Optymalność
$$
0 = \min_u \left[l_c(x, u) + \frac{\partial J^*}{\partial x} f_c(x, u) \right]
$$
$$
\Pi^* = arg \min_u [\;\;]
$$
*Widoczna jest analogia do systemu dyskretnego.*

## Pomost pomiędzy discrete, a continuous
$$
x[n+1] = f_d(x[n], u[n]) = x[n] + f_c(x[n], u[n])
$$
$$
x[n+1] \approx x[n] + h \cdot f_c(x[n], u[n])
$$
gdzie $h$ to stała czasowa *(aproksymacja Taylora)*

$$
l_d(x, u) \approx h \cdot l_c(x, u)
$$
$$
\int_0^h l_c(x, u)dt
$$
#TODO ???

$$J^*(x[n+1]) \approx J^*(x[n]) + h\frac{dJ^*}{dt}$$
z zasady łańcuchowej (chain rule)
$$\frac{dJ}{dt} = \frac{dJ}{dx} \cdot \frac{dx}{dt}$$
Wracając do równania wyżej
$$
J^*(x[n]) + h\frac{dJ^*}{dt} = J^*(x[n]) + h \frac{\partial J}{\partial x} f_c(x, u)
$$

gdzie $f_c(x, u) = \dot{x}$.

## Optymalne sterowanie
Wykorzystując pomost, oraz *równanie Bellmana* ([[Bellman equation]])
$$
J^*(s) = \min_a[l(s, a) + J^*(f(s, a))]
$$
Możemy wyznaczyć warunek optymalności:
$$
J^*(x[n]) = \min_u[l_c(x, u)h + J^*(x[n]) + h\frac{\partial J^*}{\partial x}f_c(x, u)]
$$
$$
0 = h \min_u[l_c(x, u)+ h \frac{\partial J^*}{\partial x}f_c(x, u)]
$$
I możemy pozbyć się h, jako stałej:
$$
0 = \min_u[l_c(x, u)+ \frac{\partial J^*}{\partial x}f_c(x, u)]
$$

Otrzymalismy równanie: [[Hamilton-Jacobi-Bellman equation]]

$$
u^* = \arg \min_u (HJB)
$$
$$l_c(x, u^*) = \frac{\partial J^*}{\partial x}f_c(x, u^*)$$
$$\frac{dJ^*}{dt} = -l_c(x, u^*)$$
#### Jeżeli $J, u$ spełniają HJB, to są optymalne.
## Przykład: podwójny integrator ([[double integrator]])

$\ddot{q} = u, \: l_c(q, \dot{q}, u) = q^2 + \dot{q}^2 + u^2$

$u^* = -q - \sqrt{3}\dot{q}$

$J^* = \sqrt{3} q^2 + 2q\dot{q} + \sqrt{3}\dot{q}^2$

$$
\frac{\partial J^*}{\partial x} = 
\begin{bmatrix}
2\sqrt{3}q && 2\dot{q}
\end{bmatrix}
$$
#### Z równania *HJB*
$$
(q^2 + \dot{q}^2 + u^2) + 
\begin{bmatrix}
2\sqrt{3}q && 2\dot{q} 
\end{bmatrix}
\begin{bmatrix}
\dot{q} \\
u
\end{bmatrix}
$$
$$
u^* = \arg \min_u [u^2 + (2q + 2\sqrt{3})u]
$$
#### Szukamy minimum funkcji:
$$
f'(u) = 2u + 2q + 2\sqrt{3}\dot{q}
$$
#### Widać, że $u^*$ minimalizuje funkcję.

#### Sprawdzamy czy: $J^*(u_{min}) = 0$

(Tutaj można analizować wektory własne funkcji kosztu $J^*$)

#control_theory #optimal_control #dynamic_programming




