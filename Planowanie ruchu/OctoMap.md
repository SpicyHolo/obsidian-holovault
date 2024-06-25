### Parametry
- Liczba voxeli $N \times M$ , głębokość $K$.
- Rozmiar mapy: $h \times w \times d$
- Wielkość voxela: $\frac{h}{N} \times \frac{w}{M} \times \frac{d}{K}$

 ![[octomap.png]]
### Wykorzystanie drzewa ósemkowego
*zaosczędzenie pamięci, ponieważ wolna przestrzeń nie jest dzielona na miejsze voxele*
![[octal tree.png]]
### Aktualizacja komórki
$$
P(n\lvert z_{1:t}) = \left( 
1 + \frac{1 - P(n\lvert z_t)}{P(n\lvert z_t)}
\frac{1 - P(n\lvert z_{1:t-1})}{P(n\lvert z_{1:t-1})}
\frac{P(n)}{1 - P(n)}
\right)^{-1}
$$
gdzie:
$P(n\lvert z_{1:t})$ - p. zajętości voxela $n$ 
$z_t$ - aktualny pomiar.
$P(n)$ - p. zajętości *a priori*.
$P(n\lvert z_t)$ - p. zajętości wynikające z aktualnego pomiaru.
$P(n\lvert z_{1:t-1})$ - p. zajętości w chwili $t-1$.
### Zalety
- Umiarkowanie szybka aktualizacja komórek
- logaritymiczny dostęp do komórki pamięci
- Umiarkowanie mała zajętość pamięci
- Przechowuje informacje o obiektach 3D
### Wady
- Przechowuje wyłącznie informację o zajętości *voxela*
- Dokładność reprezentacji zależna od rozmiaru *voxela*
