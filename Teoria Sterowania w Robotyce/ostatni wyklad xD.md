## Linear Programming (LP)
$O: c^Tx$, $C: Ax \leq b, Ax = b$

## Quadratic Programming (QP)
$O: x^TCx + c^Tx$, $C: Ax \leq b$

## Second-order cone prog (SOCP)
$O: f^Tx$, $C: \lVert Ax+b\lVert \leq c^Tx + d$

## Semi-define prog (SDP)
$O: f^Tx$, $C: Ax \leq b$, PSD matrix constraint

## Jak znależć f. Lapunowa cz. III xD
##### STEP 1
$\dot{x} = \alpha^T \Phi(x)$
$\alpha$ - zm. decyzyjne parametry

##### STEP 2
Szukamy $\alpha$ spełniających warunki Lapunowa
$V(x) > 0$
$\dot{V}(x) < 0$
$$
\dot{V}(x) = \frac{\partial V}{\partial x} \cdot
\frac{\partial x}{\partial t} = \alpha^T \frac{\partial \Phi(x)}{\partial x} f(x) \lvert_{x=x_i}
$$
$$
\alpha^T \Phi(x) > \xi x^tx \implies \text{asymp. stab.}
$$
$$
\alpha^T \frac{\partial \Phi(x)}{\partial x} f(x) < -\xi x^tx
$$
*nieznalezienie $\alpha$ nie znaczy, ze układ jest niestabilny*
##### Jak to zrobić dla $\forall_x$
$$
V(x) = \alpha^T \Phi^2(x) > 0, \alpha \geq 0
$$
$$
V(x) = \Phi^T(x)G\Phi(x), G \succeq 0
$$
$$
\dot{V}(x) = \frac{\partial V}{\partial x}f(x)
$$
Proponujemy funkcję: $F(x) = -Phi^T(x)H\Phi(x)$, $H\succ 0$
sprawdzamy, że:
$$
\forall_x \; \dot{V}(x) = F(x)
$$
### Przykład?
$\dot{x}=Ax$, $V(x) = x^TPx$, $P \succ 0$
$$
\dot{V}(x) = 2x^TPAx = x^TPAx + x^TA^TPx = 
x^T(PA + A^TP)x
$$
I szukamy P, dla którego $PA + A^TP < 0$

### Przykład cz.2
Jeżeli $f(x)$ wielomian i $\Phi(x)G\Phi(x) = \alpha_0 + \alpha_1 \phi_1^2(x) + \alpha_2 p_2^2$
$\frac{\partial V}{\partial x} \rightarrow \text{wielomian}$
$\Phi(x) = \begin{bmatrix} 1 && \cos(\theta) && \sin(\theta) && \dot{\theta} && \dots \end{bmatrix}$

$$
f(x) = 2 - 4x + 5x^2 = \begin{bmatrix} 1 && x \end{bmatrix}
\begin{bmatrix} p_{11} && p_{12} \\ p_{21} && p_{22} \end{bmatrix} \begin{bmatrix}1 \\ x \end{bmatrix}
$$
$\Phi = \begin{bmatrix} 1 \\ x \end{bmatrix}$, $p_{11} = 2, 2p_{12} = -4, p_{22} = 5$

### Six-hump camel
$$
p(x, y) = 4x^2 + xy - 4y^2 + 2.1x^4 + 4y^4 + \frac{x^6}{3}
$$
*Funkcja niewypukła*
$$
\min_\gamma = \gamma,p(x, y) - \gamma
$$
O ile możemy podnieść $f$ do góry, żeby można było ją przedstawić w *S.O.S. (Special Ordered Set)*.
### Region of attraction
Mamy metody $\forall_x$, a chcemy dla $x \in D \subset X$
$\implies$ Skupiamy sie na obszarze, który nas interesuje
$$
D = \left\{x \lvert g(x) \leq 0 \right\} \;\text{find}_\alpha \; p(x) + \lambda^T_\alpha(x)g(x) \text{ is SOS}
$$
$\lambda^T_\alpha$ to mnożnik Lagrange'a
$$
g(x) = 0, \lambda(x) \text{ is arbitrary}
$$
### DP /  Optimal control
- tablicowy (mesh - based approx) $\rightarrow$ nie skaluje się dobrze
- LQR (analityczne rozwiązanie $\rightarrow$ liniowy
- function approx (CNN) $\rightarrow$ sampling distribution 
- Lapunov (simpler than DP
- SOS optimizaition (10-20dim)

