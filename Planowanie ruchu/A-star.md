*Rozszerzenie algorytmu [[Dijkstra algorithm]], gdzie funkcja kosztu, zawiera **heurystykę** (funkcję estymującą koszt z węzła $n$ do celu).*
$$
f(n) = g(n) + h(n)
$$
>[!NOTE]
>Dla $h(n) = 0$ równoważny z algorytmem Dijkstry
>Zwraca rozwiązanie optymalne (jeżeli istnieje)
>Dobrze dobrana heurystyka przyspiesza znalezienie ścieżki

### Własności heurystyki
- Funkcja heurystyki powinna być mniejsza od optymalnej heurystyki
$$
h(n) \leq h^*(n)
$$
- Spójność
$$
h(n) \leq cost(o) + h(n')
$$
dla wszystkich tranzycji: $n \rightarrow^o n'$

#robotics #motion_planning #graph #algorithm 