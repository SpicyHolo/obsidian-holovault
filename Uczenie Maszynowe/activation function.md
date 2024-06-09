Funkcja aktywacji w sieci neuronowej, czyli *najczęściej* element pomiędzy sumą ważoną wejść, a wyjściem pojedynczego neuronu.

## najczęściej wykorzystywane funkcje aktywacji

- Tangens hiperboliczny:
$$f(x) = tanh(x)$$
- oraz [[sigmoid]]:
$$\sigma(x) = \frac{1}{1+e^{-x}}$$
![[sigmoid, tanh.png]]

- Aktywacja *[[ReLU]]* posiada wiele odmian, np.: *ELU, Leaky ReLU,* Swish (ReLU * sigmoid)
$$ReLU(x) =
\begin{cases} 
      x & \text{if } x > 0 \\
     0 & \text{if } x \le 0
\end{cases}
$$
	Jest prostsza do obliczenia, przyspiesza zbieżność [[SGD]].
	


#machineLearning #neuralNetwork 