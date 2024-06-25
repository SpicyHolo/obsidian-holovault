**Rapidly-exploring Random Tree$^*$**
Rozszerzenie [[RRT-star]]
*Działa tak samo jak [[RRG]], jednak w przypadku znalezienie*
*połączenia pomiędzy nowym węzłem $x_{new}$, a sąsiadami, jest ono*
*dodawane do drzewa tylko pod warunkiem, że jest krótsze niż*
*połączenie znalezione przez inny węzeł (np. $\mathbf{q}_{near}$).*

![[RRG vs RRT vs RRT-star.png]]

>[!NOTE]
> Probabilistycznie kompletny.
> Asymptotycznie optymalny.
> Złożoność: $O(\log(n)).

>[!WARNING]
>Nadaje się dla robotów nieholonomicznych ([[nonholonomic system]]), oraz robotów z ograniczeniami kinodynamicznymi ([[kinodynamic planning]]).

Po lewej na początku, po prawej po wielu iteracjach.

![[RRT-star exploring.png]]

Graf pokazuje optymalność algorytmu RRT* względem RRT

![[RRT-star optimality graph.png]]

### Przykłady wideo
![video](https://youtu.be/FAFw8DoKvik)

#robotics #motion_planning #graph #algorithm 
