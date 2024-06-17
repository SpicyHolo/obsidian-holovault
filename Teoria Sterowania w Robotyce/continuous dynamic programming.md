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

## Funkcja J*

$J^*(x[n+1]) \approx J^*(x[n]) + h\frac{dJ}{}