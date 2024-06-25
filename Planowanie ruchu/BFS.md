**(Breadth-First Search)**
*Podstawowy algorytm przeszukiwania grafu w poszukiwaniu ścieżki.*

![[BFS.gif]]
### Algorytm
- Zaczynamy w węźle powiązanym z **pozycją początkową**, dodajemy go do **kolejki** węzłów odwiedzonych.
- Dodajemy do kolejki wszystkie **węzły sąsiadujące**, które nie zostały już dodane.
- *Rozpatrujemy kolejne węzły z kolejki*, usuwając poprzednio odwiedzone.
- Kontynuuj jeżeli nie odnaleziono **węzła końcowego**, *a kolejka nie jest pusta*.

>[!NOTE]
> Oprócz znajdowania ścieżki BFS jest wykorzystywany m.in. do:
> znalezienia [[spanning tree]] - graf z usuniętymi cyklicznościami,
> sprawdzenia czy graf jest połączony

>[!IMPORTANT]
>BFS zawsze znajduję najkrótszą ścieżke (jeżeli taka istnieje)
> Złożoność obliczeniowa: $O(n)$
> Większa złożoność pamięciowa od DFS

> [!WARNING]
> Algorytm nie bierze pod uwagę kosztu przejścia pomiędzy węzłami

#robotics #motion_planning #graph #algorithm 

