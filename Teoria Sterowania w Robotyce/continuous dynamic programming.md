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

