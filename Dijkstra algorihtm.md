*Algorytm przeszukiwania grafu, gdzie przejścia mogą mieć różny koszt*.

### Algorytm
- Zaczynamy w węźle powiązanym z **pozycją początkową**, dodajemy go do **kolejki**.
- Dodajemy do kolejki wszystkich nieodwiedzonych sąsiadów i wyznaczamy dla nich długość ścieżki od startui.
- Sprawdzamy dla każdego sąsiada, czy odległość poprzez aktualny wierzchołek jest krótsza od aktualne najkrótszej drogi do sąsiada, jeżeli tak aktualizujemy ją.
- Rozpatrujemy węzeł z kolejki o najmniejszym koszcie.
- Kontynuuj jeżeli nie odnaleziono **węzła końcowego**, *a kolejka nie jest pusta*.

>[!NOTE]
> Oprócz znalezienia ścieżki BFS jest wykorzysywany m.in. do:
> testowania połączenia w grafie,
> rozwiązywania puzli, kostki rubika, itp...

>[!IMPORTANT]
>DFS nie zawsze znajduje najkrótszą ścieżkę (w przeciwieństwie do BFS)
> Złożoność obliczeniowa: $O(n)$

> [!WARNING]
> Algorytm nie bierze pod uwagę kosztu przejścia pomiędzy węzłami