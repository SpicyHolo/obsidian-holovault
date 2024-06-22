- ilośc komórek: $N \times M$
- Rozmiar mapy: $h \times w$
- Wielkość rastra $\frac{h}{N} \times \frac{w}{M}$
![[occupancy grid.png]]
*Każda komórka przechowuje informację o prawdopodobieństwie zajętości.*
- Początkowo $P = 0.5$, co oznacza komórke nieznaną.
### Aktualizacja komórki na podstawie serii pomiarów
$$
P(occ_{i, j} \lvert s^{(1)}, s^{(2)}, \dots, s^T)) = 
1 - \left(1 + \frac{P(x)}{1 - P(x)} \prod^T_{\tau=1}
\frac{P(occ_{i, j} \lvert s^{(\tau)})}{1 - P(occ_{i, j} \lvert s^{(\tau)})}
\frac{1 - P(x)}{P(x)} \right)^{-1}
$$
Gdzie rozkład $P(occ_{i, j} \lvert s^{(\tau)})$ zależy od modelu czujnika:
![[lidar uncertainty model.png]]

### Zalety
- Szybka aktualizacja komórek
- Szybki dostęp do komórek (Random Access)
- Mała zajętość pamięci
### Wady
- Przechowuje wyłącznie informację o zajętości komórki
- Brak informacji o obiektach wielopoziomowych
- Dokładność zależna od rozmiaru rastra

#robotics #motion_planning
