*Wykorzystanie programowania dynamicznego do znalezienia optymalnego sterowania.*
**(przy definicji problemu sterowania jako znalezienia ścieżki w grafie)**

## Podstawowe definicje
- dyskretne stany: $s_i \in S$
- dyskretne sterowania / akcje: $a_i \in A$
- dyskretny czas: $s[n+1] = f(s[n] + a[n])$
- jedno-krokowa funkcja kosztu: $l(s, a)$ $\rightarrow$ *odpowiada wartości na krawędzi w grafie stanów*
- koszt całkowity:  $\displaystyle{\sum^\infty_{l=1}l(s, a)}$
#### Optymalna pod-struktura
Zakładamy, że optymalizacja lokalnych, małych odcinków ścieżki, daje nam optymalną globalnie ścieżkę.

### Przykład: [[physical pendulum]]
#### Naszą sumą funkcji kosztów jest czas - t
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

#### Gdzie globalna funkcja kosztu dana jest wzorem

$$
J^*(s) = \min_{a[n]} \displaystyle{\sum^{N /\infty}_{i=0} l\left(s[i], a[i] \right)}
$$
#### A równanie przejścia do kolejnego stanu
$$
s[n+1] = f(s[n], a[n])
$$
#### Równanie Bellmana [[Bellman equation]]
$$
J^*(s) = \min_a[l(s, a) + J^*(f(s, a))]
$$

#### Optymalna polityka sterowania
$$
\Pi(s) = \arg \min_a \left[l(s, a) + J^*(f(s, a)) \right]
$$
### Algorytm [[value iteration]]
- Zaczynamy z jakimś $J$
- $\forall_s J(s) \impliedby \min_a \left[l(s, a) + J(f(s, a)) \right]$
- dzięki temu $J \rightarrow J^*$

## Problemy
- Błędy dyskretyzacji przestrzeni stanu do postaci grafu.
- Wysoka złożoność obliczeniowa, szczególnie przy *przestrzeniach wielowymiarowych*.
- Wymagana pełna znajomość stanu [[observability]].

![video](https://youtu.be/yeL7ICc8g4A)
![video2](https://youtu.be/r2bPY2s9wII)
## Ciągła wersja programowania dynamicznego ([[continuous dynamic programming]])



