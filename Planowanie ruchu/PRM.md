**(Probabilistic Road Map)**
*Algorytm poszukiwania ścieżki próbkujący przestrzeń poszukiwań*

### Algorytm
*W fazie uczenia:*
- Pobierz $n$ próbek z $\mathbb{C}_{free}$
- Połącz losowe konfiguracje używając lokalnego planera (kryterium kolizji, maksymalnej długości kroku, itp.).
*W fazie planowania ruchu:*
- Znajdź połączenia pomiędzy węzłami $\mathbf{q}_{start}$ i $\mathbf{q}_{goal}$ stosując metody przeszukiwania grafu (BFS, DFS, A-star).

![[PRM example.png]]

>[!NOTE]
> Zbudowany graf połączeń można wykorzystać do jednego planowania (single-query) lub do kilku (multi-query)

### Ograniczenia na przeszukiwanie sąsiadów
- Wyszukiwanie sąsiadów tylko w okręgu o promieniu $r$
- Tylko $K$ najbliższych sąsiadów
- Na podstawie widoczności ([[raytracing]])
### Właściwości
- Probabilistyczne kompletny ([[sampling-based search algorithms#^probabilistically-complete]]).
- Algorytm nie jest optymalnie asymptotycznie ([[asymptotically optimal]])
- Złożoność $O(n^2)$
- Wersja z ograniczeniami na sąsiadów nie jest **probabilistycznie kompletna**.

>[!WARNING]
> Problem efektywnego próbkowania przestrzeni (wąskie przejścia, w przestrzenie nieliniowej)
> 

#todo PRM inkrementalne, PRM 3D, PRM + sieci neuronowe

#robotics #motion_planning #graph #algorithm 
