**Rapidly-exploring Random Graph**

***Algorytm RRG** buduje drzewo jak [[RRT]], ale po dodaniu nowego węzła próbuje go połączyć z pozostałymi węzłami w grafie odległymi o mniej niż $r$.* 
>[!WARNING]
>W wyniku powstaje graf, który może być cykliczny.

#### Pseudokod
![[Pasted image 20240626004951.png]]
- $Steer(x_{nearest}, x_{rand})$ znajduje punkt z $x_{nearest}$ w kierunku $x_{rand}$ biorąc pod uwagę maksymalną długość kroku.
- $card(V)$ jest liczbą wierzchołków
- $\eta$ jest stałą związaną z maks. długością kroku

### Różnica pomiędzy RRT a RRG
Jeżeli uda się dodać nowy węzeł do drzewa, sprawdzane są połączenia pomiędzy nowym węzłęm, a pozostałymi wierzchołkami w grafie oddalonymi o mniej niż:
$$
r(\lvert V \lvert) = \min\left\{\gamma_{RRG}\left(\frac{\log(\lvert V \lvert)}{\lvert V \lvert} \right)^\frac{1}{d}, \eta \right\}
$$
$$
\gamma_{RRG} > \gamma^
$$