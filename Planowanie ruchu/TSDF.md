Rozszerzenie [[OctoMap]] o odległość od przeszkody
![[TSDF.png]]\
### Aktualizacja na podstawie serii pomiarów
$$
D_n(x)_{n+1} = \frac{D_n(x)w_n(x)+\hat{D_n}(x)\hat{w}(x)}{w_n(x) + \hat{w}(x)}
$$
$$
w_{n+1}(x) = \min(w_n(x) + \hat{w}(x))
$$
gdzie:
$D_N(x)_{n+1}$ - nowa wartość odległości od woksela o wsp. x
$w_n(x)$ - zakumulowana suma wag $\hat{w}(x)$, ograniczona do wartości maksymalnej.
$w(x)$ - funkcja ważąca pomiar (najczęściej stała wartośc odcinająca pomiary w części ujemnej)
