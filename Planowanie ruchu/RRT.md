**Rapidly-exploring Random Trees**
*Algorytm poszukiwania ścieżki próbkujący przestrzeń poszukiwań*

### Algorytm
- Dodajemy punkt startowy
- Losujemy nowy punkt w przestrzeni $\mathbb{C}_{free}$
- Łączymy nowy punkt z **najbliższym sąsiadem**

![[RRT diagram.png]]

### Modyfikacje
- łączenie z najbliższą krawędzią, a nie węzłem
![[nearest edge.png]]
- [[RRT-connect]] - wariancja, gdzie ścieżka rozwija się również od celu, a nie tylko startu

>[!IMPORTANT]
>Probabilistycznie kompletny, ale nie asymptotycznie optymalny

### Właściwości
- Szybko eksploruje wolną przestrzeń
- Może być użyty do planowania kinodynamicznego [[kinodynamic planning]]
- Single-query path planning w przeciwieństwie do PRM

>[!WARNING]
> Problem efektywnego próbkowania przestrzeni (wąskie przejścia, w przestrzenie nieliniowej)
> 

#robotics #motion_planning #graph #algorithm 
