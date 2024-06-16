Algorytm do wyznaczania krawędzi na obrazie, sprawdza się lepiej niż czyste wyznaczanie gradientu obrazu, np. [[sobel mask]].

### Poszczególne etapy algorytmu
1. Wstępne filtrowanie [[Gauss filter]]
2. Dla każdego piksela w obrazie wyznaczamy gradienty w dwóch głównych kierunkach
3. Na podstawie gradientu wyznaczamy moduł i kierunek gradientu.
4. *Dla każdego punktu  sprawdzamy najbliższe dwa punkty sąsiadujące, leżące na kierunku obliczonego gradientu.*
5. *Jeśli rozpatrywany piksel ma maksimum funkcji obrazowej w tej trójce pikseli, piksel jest wygaszany w obrazie wynikowym, w przeciwnym razie jest pozostawiany.*

