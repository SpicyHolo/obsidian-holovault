Źródło[^1]
*Algorytm poszukiwania ścieżki próbkujący przestrzeń poszukiwań*
![[incremental search example.png]]
### Algorytm
- **Inicjalizacja** - utwórz zbiór losowych pozycji dopuszczalnych będących w $\mathbb{C}_{free}$ zawierających $\mathbf{q}_{start}$ i $\mathbf{q}_{goal}$.
- **Wybierz wierzchołek** $\mathbf{q}_{cur}$ do analizy
- **Zaplanuj lokalną ścieżkę** pomiędzy węzłem $\mathbf{q}_{cur}$, a losowym węzłem $\mathbf{q}_{new}$. Jeżeli nie udało się zaplanować ścieżki lokalnej, idź do punktu 2.
- **Dodaj krawędź do grafu** między węzłem $\mathbf{q}_{cur}$, a losowym węzłem $\mathbf{q}_{new}$. Dodaj nowy węzeł do grafu.
- Jeżeli nie udało się zaplanować ścieżki globalnej idź do punktu 2.



>[!NOTE]
> Zbudowany graf połączeń można wykorzystać do jednego planowania (single-query) lub do kilku (multi-query)

### Ograniczenia na przeszukiwanie sąsiadów
- Wyszukiwanie sąsiadów tylko w okręgu o promieniu $r$
- Tylko $K$ najbliższych sąsiadów
- Na podstawie widoczności ([[raytracing]])

>[!IMPORTANT]
> Znaleziona ścieżka nie jest optymalna, ale wraz z ilością próbek $n$, zbliża się do optimum (algorytm optymalny asymptotycznie)

### Właściwości
- Probabilistyczne kompletny ([[sampling-based search algorithms#^probabilistically-complete]]).
- Algorytm optymalnie asymptotycznie ([[asymptotically optimal]])
- Złożoność $O(n^2)$
- Wersja z ograniczeniami na sąsiadów nie jest **probabilistycznie kompletna**.

>[!WARNING]
> Problem efektywnego próbkowania przestrzeni (wąskie przejścia, w przestrzenie nieliniowej)
> 

#todo PRM inkrementalne, PRM 3D, PRM + sieci neuronowe

[^1]:S. M. LaValle, Planning Algorithms (2006), Chapter 5.4

#robotics #motion_planning #graph #algorithm 