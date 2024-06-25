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
Jeżeli uda się dodać nowy węzeł do drzewa, sprawdzane są połączenia pomiędzy nowym węzłem, a pozostałymi wierzchołkami w grafie oddalonymi o mniej niż:
$$
r(\lvert V \lvert) = \min\left\{\gamma_{RRG}\left(\frac{\log(\lvert V \lvert)}{\lvert V \lvert} \right)^\frac{1}{d}, \eta \right\}
$$
$$
\gamma_{RRG} > \gamma^*_{RRG} = 2(1 + \frac{1}{d})^\frac{1}{d}
\left(\frac{\mu(\mathbb{R}_{free})}{\zeta_d} \right)^\frac{1}{d}
$$
![[RRT vs RRG.png]]

>[!NOTE]
> Probabilistycznie kompletny.
> Asymptotycznie optymalny.
> Złożoność: $O(\log(n)).

>[!WARNING]
>Nie nadaje się do robotów nieholonomicznych, oraz robotów z ograniczeniami kinodynamicznymi.



#robotics #motion_planning #graph #algorithm 
