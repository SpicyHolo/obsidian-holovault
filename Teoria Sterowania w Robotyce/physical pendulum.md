**Wahadło fizyczne**
Model dynamiczny wahadła fizycznego, jest układem nieliniowym ([[nonlinear system]]).

### Równania dynamiki
$$
T = \frac{1}{2} ml\cdot\dot{\theta}^2 
$$
$$
V = mgl \cdot \cos(\theta)
$$
$$
\mathcal{L} = T-V
$$
$$
\frac{d}{dt}\left(\frac{\partial \mathcal{L}}{\partial\dot{q}}\right) -
\frac{\partial \mathcal{L}}{\partial q} = 
Q = \tau - R
$$
$$
ml^2\ddot{\theta} + b\dot{\theta}+mgl\cdot\sin(\theta) = \tau
$$
### Uproszczenie do układu 1-go rzędu
Zakładamy: 
$$ml^2\ddot{\theta} \ll b\theta \implies b\dot{\theta} + mgl \cdot \sin(\theta) = \tau$$
$$
\dot{x} = \frac{1}{b} [u-mgl\cdot sin(x)]
$$
![[physical pendulum, overdamped.png]]

### Pełny obraz fazowy
$$
\dot{x} = f(\dot{x}, x) = 
\begin{bmatrix}
\theta \\
\frac{1}{ml^2} \left[ u - b\cdot\theta - mgl\cdot\sin(\theta)\right]
\end{bmatrix}
$$
Dla $b = 0, u = 0 \implies \ddot{\theta} = \frac{g}{l} \sin(\theta)$

![[physical-pendulum-phase-picture.png]]


#control_theory 
