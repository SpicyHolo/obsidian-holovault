**Drzewa k-d** pozwalają na efektywne wyszukiwanie najbliższego sąsiada w przestrzeni. Są wykorzystywane m.in. w algorytmie [[PRM-star]].

![[kd trees.png]]

### Algorytm
- Dziel przestrzeń na dwa podzbiory po kolejnych wymiarach, za pomocą hiperpłaszczyznę, wybierając medianę dla danego wymiaru (punkt środkowy).
-  Twórz drzewo binarne, którego kolejnymi węzłami są punkty środkowe.
**Przeszukiwanie drzewa**
- Przeszukuj drzewo korzystając z [[DFS]] i zapisuj najbliższy punkt i minimalną odległość $r_{min}$.
- Eliminuj całe fragmenty drzewa wykorzystując fakt, że jeżeli aktualny promień $r$ nie przecina hiperpłaszczyzny, to lewa lub prawa część grafu nie musi być przeszukiwana.

#algorithm #graph #robotics #motion_planning 
