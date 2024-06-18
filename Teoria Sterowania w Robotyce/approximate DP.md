Aproksymacja Dynamic Programming powstała w wyniku problemów skalowalności klasycznych metod przeszukiwań w DP ([[continuous dynamic programming]])

Dla systemów wielowymiarowych rozmiar przeszukiwanego grafu szybko staje się zbyt duży.

Rozwiązaniem jest aproksymacja funkcji kosztu.
## Tabela wartości
$$
\forall_{s_i \in S} \;
\hat{J}(x) <= \min_a \left[
l(s_i, a) + \hat{J}\left(f(a, s_i)\right)
\right]$$


## Sieć neuronowa ([[neural network]])
$$J_\alpha(x)$$
##### Step 1
Losujemy $x_i \in x_s \subset X$, $u_j \in U_s \subset U$
$$
\forall_{i, j} \;\dot{x}_{ij} = f(x_i, u_j)
$$
$$
l_{ij} = l(x_i, u_j)
$$
$$
J^d_i = \min_j \left[l_{ij} + \hat{J}_\alpha(\dot{x}_{ij}) \right]$$
##### Step 2
$$
\arg \min_\alpha \sum \left[\hat{J_\alpha}(x_i) - J^d_i\right]^2
$$
$$
\arg \min_\alpha \sum \left[\hat{J_\alpha}(x_i) - 
\min_j \left(l_{ij} + \hat{J_\alpha}(x_{ij}) \right)
\right]^2
$$
$$
\arg \min_\alpha \sum \left[\hat{J_\alpha}(x_i) - 
\min_j \left(l_{ij} + \hat{J_\beta}(x_{ij}) \right)
\right]^2
$$
gdzie $\beta = LPS(\alpha)$ (Target network?)

#### On-policy sampling
Próbkowanie $\rightarrow$ sieć się uaktualnia w okolicy

### Zbieżność sieci ADP
$$
\hat{J}_\alpha(x) = \alpha^T \Phi(x)
$$
$\Phi$ - transformata nieliniowa cech wejściowych
$$
\arg \min_\alpha \sum_i \left[\alpha^T \Phi(x) - J^d_i \right]^2
$$
##### Podobne do kwadratowej funkcji kosztu ([[LQR controller]])
$$
\hat{J}_\alpha(x) = \alpha^T \Phi(x) \iff J^*(x) = x^TSx
$$

$$
loss = \sum_i \left[x^T \hat{S}x - J^d_i \right]
$$
$$
\hat{S} = \hat{S} - \eta \frac{\partial loss}{\partial \hat{S}}
$$
**Ten pomysł nie działa, ze względu na nieskończony horyzont czasowy LQR**
### Discounting of ADP
$$
L = \sum^\infty_{n=0} \gamma^n l(x[n], u[n])
$$
$\gamma \in (0; 1]$ - Dzięki temu błędy w przyszłości mają mniejszą wagę
### Przykład dla LQR 
([[LQR controller]])

$$
\sum^\infty_{i=0} \gamma^i l(x, u)
$$
Równoważny LQRowi =
$$[k, S] = LQR(\sqrt{\gamma}A, B, Q, \frac{R}{\gamma})
$$
*W konsekwencji mamy juz inny od początkowego układ.*

