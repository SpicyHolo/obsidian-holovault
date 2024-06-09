Sieć neuronowa składa się z podstawowego modelu neuronu ([[neuron model]])

![[activation-function.png]]

Składa się z sumy ważonej wejść, [[activation function]], dodatkowo stosuje się stałą tzw. *bias* (nie ma na schemacie), z funkcji aktywacji bezpośrednio mamy wyjście z neuronu

### Sieci neuronowe

Neurony składają się na warstwy; warstwy łączą się między sobą, tworząc sieci.

![[neural network model.png]]

Wyróżniamy:
- *[[input layer]]*
- *[[hidden layer]]*
- *[[output layer]]*

Sieci w pełni połączone są najbardziej efektywnym rozwiązaniem dla wielu zastosowań (np. jako [[classifiers]]) .
Ale więcej parametrów, oznacza trudniejsze i wolniejsze uczenie.

### Sieci konwolucyjne - *[[CNN]]*

Szczególnie przydatne w przetwarzaniu obrazów


### Pierwszy model neuronu (w 1958r.) - *[[perceptron]]*

$$f(x) =
\begin{cases} 
      1 & \text{if } w \cdot x + b > 0 \\
     0 & \text{otherwise} 
\end{cases}
$$
Prosty model z wagą $w$ , biasem $b$. 

### Uczczenie sieci wielowarstwowych 
- Stosuje się algorytm: *[[backpropagation]]*
- Podział uczenia na Epoki [[epoch]] (epoka odpowiada podaniu na wejściu całego zbioru uczącego)
- Definiuje się kryterium zatrzymania (np. dokładność / [[cost function]] na zbiorze walidacyjnym, nie polepszy się przez 10 epok)
- Wartość stałej uczenia można zmieniać wg harmonogramu, albo warunkó w

### Impulsowe sieci neuronowe - *[[spiking neural network]]*
Bardziej zbliżone do mechanizmu działania biologicznych sieci neuronowych.
https://arxiv.org/pdf/1804.08150



#machineLearning #neuralNetwork