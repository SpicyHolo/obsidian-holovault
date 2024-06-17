*(Układ dynamiczny)*
Opis matematyczny rzeczywistego zjawiska, którego ewolucja jest wyznaczana jednoznacznie przez *stan początkowy* $x_0$, najczęściej opisany *wektorowym równaniem różniczkowym.*

## System nieliniowy ([[nonlinear system]])
*Najbardziej ogólny opis układu:*
$$
\dot{x} = f(x, u)
$$
$$
y = g(x)
$$

## System 2-go rzędu ([[second-order system]])
Zwykle w fizyce spotykamy się z układami 2-go rzędu, czyli:
$$
x = 
\begin{bmatrix}
q \\
\dot{q}
\end{bmatrix}, \;\;
\ddot{q} = f(q, \dot{q}, u)
$$
## Układ afiniczny ([[control-affine system]])
**(względem sterowania)**
Specjalna klasa systemów nieliniowych, gdzie system jest liniowo zależny od sterowania:
$$
\ddot{q} = f_1(q, \dot{q}) + f_2(q, \dot{q})\cdot u
$$
## Układ liniowy ([[linear system]])
Bardzo uproszczony model systemu dynamicznego
$$
\dot{x} = Ax+Bu
$$
$$
y = Cx+Du
$$

### Sterowalność układu afinicznego [[controllability]]
Układ afiniczny jest sterowalny, gdy $f_2(q, \dot{q})$ jest *pełnego rzędu wierszowego*.

## Model dynamiki robota ([[robot dynamics]])
Podstawowy model dynamiki robota:
$$
M(q)\cdot\ddot{q}+C(q, \dot{q})\cdot\dot{q}+G(q) = B\cdot\tau \\
$$
$$
\ddot{q} = M^{-1}(q)\cdot
\left[ B\cdot\tau - C\cdot\dot{q} - G \right]
$$
$M(q)$ zawiera masy, $C(q, \dot{q}])$ siły Coriollisa, $G(q)$ siły grawitacji, $B$ wpływ sterowania.



#control_theory
