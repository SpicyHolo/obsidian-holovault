Sterownik liniowo-kwadraowy (linear-qudaratic regulator), sterownik minimalizujący kwadratową funkcję kosztu. Gwarantuje optymalne sterowanie, dla układów liniowych ([[linear system]]).
### Funkcja kosztu LQR
$$
l(x, u) = x^TQx + u^TRu
$$
gdzie macierze $Q$ oraz $R$ są odpowiednio dodatno i półdodatnio określone, obie symetryczne
#TODO (are Q, R symmetric?)
$$
Q \succeq 0, R \succ 0 
$$
*Intuicyjnie macierz $Q$, mówi o koszcie nie bycia w żądanym stanie, a macierz $R$ o koszcie sterowania.*
### Suma kosztów $J^*$
$$
L = \int^\infty_0 l(x, u) dt 
$$
$$
J^* = x^TSx
$$
gdzie $S$ to macierz symetryczna, dodatnio-określona ($S^T = S$, $S \succ 0$)
$$
\frac{\partial J^*}{\partial x} = 2x^TS
$$
$$
0 = \min_u \left[l(x, u)  + \frac{\partial J^*}{\partial x}f(x, u) \right]
$$
$$
0 = \min_u \left[x^TQx + u^TRu + 2x^TS(Ax + Bu) \right]
$$
Pozbywając się składników niezależnych od $u$:
$$
0 = \min_u \left[u^TRu + 2x^TS(Bu) \right]
$$
Szukamy sterowania spełniającego  [[Hamilton-Jacobi-Bellman equation]]
$$
\frac{\partial J}{\partial u} =
2u^TR + 2x^TSB = 0
$$
$$
u^TR + x^TSB = 0
$$
$$
u^T = -x^TSBR^{-1}
$$
$$
u^* = -R^{-1}B^TSx
$$
Szukamy macierzy $S$ z warunku koniecznego **HJB**
$$
x^TQx + u^TRu + 2x^TS(Ax + Bu)
$$
$$
x^TQx+x^TSBR^{-1}RR^{-1}B^TSx + 2x^TS\left(Ax-BR^{-1}B^TSx \right)= 0
$$
$$
x^T \left(Q + SBR^{-1}B^TS + 2SA-2SBR^{-1}B^TS\right)\,x
$$
$$
Q + SBR^{-1}B^TS + 2SA - 2SBR^{-1} B^TS = 0
$$
$$
x^T(Q - SBR^{-1}B^TS + 2SA)x
$$
gdzie $x^T(SA)x =x^T(A^TS)x$ *(ponieważ to skalar)*
$$
x^T(Q-SBR^{-1}B^TS + SA + A^TS)
$$
Czyli tzw. ciągłe algebraiczne równanie Ricattiego 
([[continuous algebraic Ricatti equation]])

### Dla każdej macierzy $Q$, $R$ układ jest stabilny, jeśli jest stabilizowalny.



