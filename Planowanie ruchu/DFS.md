**(Depth-First Search)**
*Podstawowy algorytm przeszukiwania grafu w poszukiwaniu ścieżki.*
![[DFS.gif]]
### Algorytm
- Zaczynamy w węźle powiązanym z **pozycją początkową**, dodajemy go do **stosu** węzłów odwiedzonych.
- Dodajemy do stosu pierwszego nieodwiedzonego sąsiada.
- *Rozpatrujemy kolejne węzły ze stosu, usuwając poprzednio odwiedzone.
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

#robotics #motion_planning #graph #algorithm 