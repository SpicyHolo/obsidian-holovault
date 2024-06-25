Układy nieliniowe ([[nonlinear system]]) można przybliżyć za pomocą układów liniowych ([[linear system]]), wokół punktu pracy:

$$
\displaystyle{
\dot{x} \approx f(x_0, u_0) + \frac{\partial f}{\partial x}
\lvert_{x=x_0, u=u_0}
(x - x_0) + \frac{\partial f}{\partial u}
\lvert_{x = x_0, u=u+0} 
(u - u_0)
}
$$

## Przykład linearyzacji
Wahadło fizyczne ([[physical pendulum]])

$$ml^2\ddot{\theta} + b\dot{\theta} + mgl \cdot \sin(\theta) = \tau$$
$x =\begin{bmatrix} \theta \\ \dot{\theta} \end{bmatrix}$, $\tau = u$
Punkt pracy:
$\theta_0 = \pi$, $\dot{\theta}_0 = 0$, $u_0 = 0$

$$
\dot{x} = \begin{bmatrix}
\dot{\theta} \\
\frac{1}{ml^2} \left(\tau - b\dot{\theta} - mgl \cdot \sin(\theta) \right) \\
\end{bmatrix}
$$
$$
A = \begin{bmatrix}
0 && 1 \\
-\frac{g}{l} && -\frac{b}{ml^2} \\
\end{bmatrix}
$$
$$
B = \begin{bmatrix}
0 \\
\frac{1}{ml^2}
\end{bmatrix}
$$
## Analiza wektorów własnych
dla $m = 1$, $l = 1$, $b = 0$, $g = 10$
$$\hat{\dot{x}} = \begin{bmatrix}
0 && 1 \\
10 && 0 \\
\end{bmatrix}\hat{x} + \begin{bmatrix}
0 \\
1
\end{bmatrix}\hat{u}
$$
Zakładamy $u \approx 0$

$\lambda_1 = \sqrt{10}$, $\lambda_2 = -\sqrt{10}$
$v_1 = \begin{bmatrix} 1 \\ \sqrt{10} \end{bmatrix}$, $v_2 = \begin{bmatrix} -1 \\ \sqrt{10} \end{bmatrix}$
$$
\hat{x} = \alpha_1 v_1 + \alpha_2 v_2
$$
$$
\hat{\dot{x}} = Ax = \lambda_1 \alpha_1 v_1 + \lambda_2 \alpha_2 v_2
$$
![[pendulum-taylor.png]]

