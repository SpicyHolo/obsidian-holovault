*Algorytm przeszukiwania grafu **(kompletny, optymalny)**, gdzie przejścia pomiędzy węzłami mogą mieć różny koszt*.
![[W3_SS_Dijkstra_1.webp]]
### Algorytm
- Zaczynamy w węźle powiązanym z **pozycją początkową**, dodajemy go do **kolejki**.
- Dodajemy do kolejki wszystkich nieodwiedzonych sąsiadów i wyznaczamy dla nich długość ścieżki od startu.
- Sprawdzamy dla każdego sąsiada, czy odległość poprzez aktualny wierzchołek jest krótsza od aktualne najkrótszej drogi do sąsiada, jeżeli tak aktualizujemy ją.
- Rozpatrujemy węzeł z kolejki o najmniejszym koszcie.
- Kontynuuj jeżeli nie odnaleziono **węzła końcowego**, *a kolejka nie jest pusta*.
*Rozpatrując wpierw wierzchołki o najmniejszym koszcie, algorytm gwarantuje znalezienie najkrótszej ścieżki.*

>[!NOTE]
> Złożoność obliczeniowa wynosi $O(\lvert V\lvert^2)^1$,
> Przy użyciu [[priority queue]]$: (\lvert E \lvert + \lvert V \lvert + \log \lvert V \lvert )$

#robotics #motion_planning #graph #algorithm 
