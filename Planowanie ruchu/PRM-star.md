*Asymptotycznie optymalny wariant algorytmu [[PRM]].*
>[!IMPORTANT]
> tzn., znaleziona ścieżka nie jest optymalna, ale wraz z rosnącą ilością próbek $n$, zbliża się do optimum (algorytm optymalny asymptotycznie)

![[PRM-star.png]]
### Dynamiczna zmiana promienia $r$
W wariancie, gdzie [[PRM]] podczas łączenia bierze pod uwagę wierzchołki w promieniu $r$ od nowego wierzchołka.
$$
r = \gamma_{PRM}\left(\frac{\log(n)}{n}^{\frac{1}{d}}\right)
$$
Parametr $\gamma_{PRM}$ dobieramy na podstawie:
$$\gamma_{PRM} > \gamma^*_{PRM}$ = 
2\left(1 + \frac{1}{d}\right)^{\frac{1}{d}} 
\left(\frac{\mu(\mathbb{R}_{free})}{\zeta_d} \right)^\frac{1}{d}
$$
Gdzie $d$ - wymiarowość problemu, $\mu(\mathbb{R}_{free})$ jest miarą Lebesgue'a (objętość) przestrzeni wolnej od kolizji, $\zeta_d$ jest objętością kuli jednostkowej w $d$-wymiarowej przestrzeni.

### K najbliższych sąsiadów
$$
k(n) = k_{PRM}(\log(n))
$$
gdzie parametr ${k_{PRM}}$ dobieramy na podstawie:
$$
k_{PRM} > k^*_{PRM} = e\left(1 + \frac{1}{d}\right)
$$
$d$ to wymiarowość problemu, a $e$ to podstawa logarytmu naturalnego
