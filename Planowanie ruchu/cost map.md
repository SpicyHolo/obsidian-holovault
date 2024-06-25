Mapa kosztów definiowana najczęściej na podstawie mapy wysokościowej ([[elevation map]]). Koszt zależy od:
- ukształtowania terenu (wysokościm nachylenia, lokalnej wariancji wysokości, krzywizny, itp.)
- rodzaju terenu
- właściwości robota
 ![[cost map 1.png]]
 ![[cost map 2.png]]
 ![[cost map 3.png]]
#robotics #motion_planning 

### Przykład
Koszt przejścia pomiędzy komórkami:
$$
c = c_1 + c_2
$$
$$
c1 = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2 + (z_1 - z_2)^2}
$$
*(odległość euklidesowa)*
$$
c2 = 1 - \frac{\sqrt{\sum^N_{i=0}(x^n_i)^2} + \sum^N_{i=0}(y^n_i)^2 + \sum^N_{i=0}(z^n_i)^2}
{N}
$$
(*wariancja sferyczna z wektorów normalnych* $p^n$ *do powierzchni terenu w otoczeniu rozważanego punktu*)

### Przykład 2
Wariancja 3D jako przybliżenie kosztu
$$
\sum = var(X) = E((X-\mu)(X - \mu)^T) \in \mathbf{R}^{m \times m} \text{ where } \mu = E(X) \in \mathbf{R}^m
$$
$$
M = \begin{bmatrix} 
\dots && x_k  - \bar{x} && \dots \\
\dots && y_k  - \bar{y} && \dots \\
\dots && z_k  - \bar{z} && \dots \\
\end{bmatrix} \in \mathbf{R}^{3 \times n}
$$
$$
S = \frac{1}{n}MM^T \in \mathbf{R}^{3 \times 3}
$$
#todo fix R to be real numbers
#todo filmiki odnosnie wariancji

