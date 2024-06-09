### **Convolutional neural networks**

- Konwolucyjne sieci neuronowe, każdy neuron w poprzedniej warstwie jest podłączony do każdego neuronu w kolejnej warstwie.
- Wyjście sieci jest typu [[softmax]], czyli wektor sumuje się do $1$ , a wartości: $x \in [0, 1]$, co można interpretować jako prawdopodobieństwo przynależności do klasy ([[classifiers]]).  
$$f(Z)_j = \frac{\displaystyle e^{Z_j}}{\displaystyle \sum_{k=1}^K e^{Z_k}}$$
#machineLearning #neuralNetwork