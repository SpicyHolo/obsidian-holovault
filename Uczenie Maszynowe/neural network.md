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

### Uczenie sieci [[network training]]

### Impulsowe sieci neuronowe - *[[spiking neural network]]*
Bardziej zbliżone do mechanizmu działania biologicznych sieci neuronowych.
https://arxiv.org/pdf/1804.08150

### Sieci rekurencyjne [[RNN]]


#machineLearning #neuralNetwork