*Wykorzystanie programowania dynamicznego do znalezienia optymalnego sterowania.*
**(przy definicji problemu sterowania jako znalezienia ścieżki w grafie)**

### Podstawowe definicje
- dyskretne stany: $s_i \in S$
- dyskretne sterowania / akcje: $a_i \in A$
- dyskretny czas: $s[n+1] = f(s[n] + a[n])$
- jedno-krokowa funkcja kosztu: $l(s, a)$ $\rightarrow$ *odpowiada wartości na krawędzi w grafie stanów*
- koszt całkowity:  $\displaystyle{\sum^\infty_{l=1}l(s, a)}$
#### optymalna pod-struktura
Zakładamy, że optymalizacja lokalnych, małych odcinków ścieżki, daje nam optymalną globalnie ścieżkę.

## Przykład: [[physical pendulum]]
Funkcja kosztu -- czas t
$$
t = \displaystyle{
\sum^N_{i=0} l(s, a)
}
$$
$$
l(s,a) =
\begin{cases}
1 \text{ if } s \neq s_{g} \\
0 \text{ if } s = s_{g}
\end{cases}
$$
gdzie $s_g$ - stan docelowy.

$$
I^*(s) = \min_{a[n]} \displaystyle{\sum^{N /\infty}_{i=0} l\left(s[i], a[i] \right)}
$$
A równanie przejścia do 
$$
s[n+1] = f(s[n], a[n])
$$




