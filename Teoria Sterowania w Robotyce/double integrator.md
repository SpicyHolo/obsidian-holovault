Podwójny integrator, jeden z najprostszych systemów liniowych ([[linear system]]).
$$
\ddot{q} = u
$$
### Sterowanie optymalne, minimalizacja czasu
$$
\lvert u \lvert <1
$$
#### Pomysł na sterowanie:
- Gaz do dechy
- Hamulec

$\ddot{q} = -1 / \int dt$
$\dot{q} = \dot{q}_0  -t$ (1)

$t = \dot{q}_0 - \dot{q}$ (2)

from (1)
$$q = \dot{q}_0t + q_0 - \frac{1}{2}t^2$$

from(2)
$$q = \dot{q}_0 (\dot{q}_0 - \dot{q}) + q_0 - \frac{1}{2}(\dot{q}_0 - \dot{q})^2$$
$$q = \dot{q}_0^2 - \frac{1}{2}\dot{q}_0 + q_0 - \frac{1}{2}\dot{q}^2$$

$$
q(t) = C - \frac{1}{2} \dot{q}^2
$$
#### Wykres sterowania
![[double-integrator-controller.png]]










#control_theory 