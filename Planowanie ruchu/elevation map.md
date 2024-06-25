### Parametry:
- Liczba komórek: $N \times M$
- Rozmiar mapy: $h \times w$
- Wielkość rastra: $\frac{h}{N} \times \frac{w}{M}$
![[elevation map.png]]*Każda komórka przechowuje informację o wysokości.*
- Aktualizacja: $h_{i, j} =\ max(s^{(1)}, s^{(2)}, \dots, s^T)$
- Tracimy informację o przestrzeni pod obiektami!
### Zalety
- szybka aktualizacja komórek
- szybki dostęp do koórek
- mała zajętość pamięci
### Wady
- tylko informacja o wysokości komórki
- dokładność zależna od rozmiaru rastra
- brak informacji o obiektach wielopoziomowych
### Rozszerzenia
- Mapa wielopoziomowa
- Powiązanie z mapą kategorii (np. rodzaju terenu)

#robotics #motion_planning 