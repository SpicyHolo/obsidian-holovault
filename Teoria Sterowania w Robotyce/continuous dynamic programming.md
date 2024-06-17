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
O = \min_u \left[l_c(x, u) + \frac{\partial J^*}{\partial x} f_c(x, u) \right]
$$
$$
\Pi^* = arg \min_u O
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
O = h \min_u[l_c(x, u)+ ]
$$
