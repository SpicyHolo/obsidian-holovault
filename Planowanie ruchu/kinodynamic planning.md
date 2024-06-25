### Metody próbkujące przestrzeń sterowań / stanów
>[!WARNING]
>Przeszukiwanie przestrzeni stanu, która dla obiektów
dynamicznych jest przestrzenią wielowymiarową, nie jest
efektywnym rozwiązaniem.

*Rozwiązaniem może być próbkowanie przestrzeni sterowań (shooting methods) i symulowanie obiektu z użyciem modelu dynamiki.*

### Próbkowanie sterowania $u(t)$
- Wybierz sterowanie $u(t)$.
 - Korzystając z modelu dynamiki modeluj zachowanie obiektu pod wpływem sterowania $u(t)$.
- Podczas modelowania trajektorii obiektu sprawdzaj ograniczenia ruchu (w tym kolizje z obiektami).
- Określ jakość uzyskanej trajektorii (np. czy jest wolna od kolizji i czy zbliża robota do celu.

[!WARNING]