Algorytm uczenia wielowarstwowych sieci neuronowych

- Wprowadzamy funkcje kosztu i możliwość prześledzenia gradientów wstecz, od wyjścia sieci na jej wejście.
- Każda modyfikacja parametru jest składową wektora w wielowymiarowej przestrzeni

### [[MSE]] (mean square error)

W ogólności funkcja kosztu [[cost function]] (błąd średnio kwadratowy):
$$ J = \frac{1}{N} \displaystyle\sum_{i=1}^{N} (y_i - \hat{y}_i)^2 $$
Na podstawie błędu wyznaczamy aktualizacje dla każdej z wag, na podstawie kierunku lokalnego gradientu .
$$\frac{\partial J}{\partial w_i}$$
W sumie są trzy składowe wektora kierunku gradientu: *pochodna funkcji strat po jednym z wyjść, pochodna wyjścia po aktywacji, pochodna aktywacji po wejściu (wadze) neuronu.*
$$\frac{\partial J}{\partial w_i} = \frac{\partial J}{\partial o_i} \frac{\partial o_i}{\partial a} \frac{\partial a}{\partial w_i}$$
Wykorzystujemy [[chain rule]], do wyznaczenia kierunku spadku gradientu.

![[backpropagation gradient.png]]



### Problem lokalnego minima
Poruszanie się w kierunku spadku gradientu powoduje utykanie w lokalnych minimach funkcji.
Rozwiązaniem problemu jest dodanie momentu, do składowej wektora
$$\theta=\theta-\eta \cdot\nabla_\theta \, J(\theta) \text{ - wersja bez momentu}$$
$$
\begin{cases}
v_t=\gamma \cdot v_{t-1} + \eta \cdot\nabla_\theta \, J(\theta) \\
\theta = \theta - v_t 
\end{cases} \;\text{ - wersja z momentem}$$
$\eta$ - stała uczenia, $J$ - funkcja kosztu, $\theta$ - parametry

### Algorytm [[ADAM]] (Adaptive Moment Estimation)
Adaptacyjnie dostosowuj wartość momentu.


#machineLearning #neuralNetwork