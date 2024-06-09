Lepszy niż algorytm **k-średnich** ([[k-means algorithm]]), lepiej radzi sobie z grupami, które nie są wypukłe.

![[dbscan.png]]

W odróżnieniu od k-średnich, zdobywanie terenu odbywa się małymi porcjami przestrzeni, lokalnie.
Na zasadzie bliskości do sąsiedztwa już zaliczonego do jakiejś grupy
### Działanie algorytmu
1. Wybieramy losowo nieodwiedzony punkt i wyznaczamy wszystkie punkty w sąsiedztwie $\varepsilon$.
2. Punkt traktujemy jako początek grupy, jeżeli w sąsiedztwie znajduje się określona minimalna ilość sąsiadów.
3.  Wszystkie punkty w sąsiedztwie są przypisywane do grupy.
4. Powtarzamy, aż wszystkie punkty będą odwiedzone
