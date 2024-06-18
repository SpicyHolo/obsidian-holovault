Funkcja Lapunowa służy do udowadniania stabilności  ([[stability of dynamical system]]) układów nieliniowych ([[nonlinear system]]).

## Przykład dla wahadła
([[physical pendulum]])
z tarciem...
$$
ml^2 \ddot{\theta} + mgl \sin(\theta) = -b\dot{\theta}
$$

$T = \frac{1}{2}ml^2 \dot{\theta}^2$, $V = -mgl \cos(\theta)$
$$
E = T + V = \frac{1}{2}ml^2 \dot{\theta}^2 -mgl \cos(\theta)
$$
$$
\frac{d}{dt}E(x) = \frac{\partial E}{x}\dot{x} =
\frac{\partial E}{\partial \theta}\dot{\theta} +
\frac{\partial E}{\partial \dot{\theta}}\ddot{\theta} =
$$
$$
= \dot{\theta}mgl \sin(\theta) + ml^2 \dot{\theta}\ddot{\theta} = \dot{\theta}\left(mgl \sin(\theta) + ml^2 \ddot{\theta} \right) =
$$
Z równania dynamiki wahadła:
$$
= \dot{\theta} - b\dot{\theta} = -b\dot{\theta}^2
$$
##### Stabilność w $x = 0$, warunki Lapunova
$$
V(x) = E(x) + mgl
$$
$$
\dot{V}(x) = \dot{E}(x) = -b\dot{\theta}
$$
$V(0) = 0, \forall_x \neq 0 \; V(x)>0$
$\dot{V}(0) = 0, \forall_{x \neq 0 } \dot{V}(x) \leq 0$
*Co daje nam stabilność w sesie Lapunova*\

#control_theory 

