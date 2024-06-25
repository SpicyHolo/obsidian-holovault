### Metody próbkujące przestrzeń sterowań / stanów
>[!WARNING]
>Przeszukiwanie przestrzeni stanu, która dla obiektów
dynamicznych jest przestrzenią wielowymiarową, nie jest
efektywnym rozwiązaniem.
Dodatkowo wymaga znajomości modelu odwrotnego dynamiki.

*Rozwiązaniem może być próbkowanie przestrzeni sterowań (shooting methods) i symulowanie obiektu z użyciem modelu dynamiki.*

### Próbkowanie sterowania $u(t)$
- Wybierz sterowanie $u(t)$.
 - Korzystając z modelu dynamiki modeluj zachowanie obiektu pod wpływem sterowania $u(t)$.
- Podczas modelowania trajektorii obiektu sprawdzaj ograniczenia ruchu (w tym kolizje z obiektami).
- Określ jakość uzyskanej trajektorii (np. czy jest wolna od kolizji i czy zbliża robota do celu.

>[!WARNING]
>Niewielka zmiana sterowania może powodować duże zmiany w konfiguracji robota

>[!IMPORTANT]
>W metodach próbkujących sterowanie, stan wybór najbliższego sąsiada jest niedokładnie zdefiniowany.

![[randomized Kinodynamic planning.png]]

### Pseudokod
![[planowanie kinodynamiczne psuedokod.png]]
*Stan próbkowany jest z **przestrzeni kienematycznej**.* 
*Funkcja* **NEW_STATE()** *znajduje trajektorię w kierunku do zadanego punktu próbkując sterowanie i biorąc pod uwagę model dynamiczny robota.*

![[3D kinodynamic planning.png]]

### Przykłady:
- [xwing](https://lavalle.pl/rrt/gallery_xwing.html)
- [3d grid](https://lavalle.pl/rrt/gallery_3dgrid.html)
- [lunar](https://lavalle.pl/rrt/gallery_lunar.html)
- [trailer](http://lavalle.pl/rrt/gallery_trailer.html)
### Problemy i właściwości
>[!NOTE]
> Można wykluczać węzły, które powodują kolizję (Inevitable Collision States)
> Konieczne jest dobranie czasu symulacji $T$ i czasu próbkowanie $\Delta t$
> Wykorzystanie metod optymalizacji, do wyznaczenia sterowania.

