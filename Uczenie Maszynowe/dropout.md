Metoda poprawiająca uczenie i wyniki sieci neuronowej.
Polega na losowym wyłączaniu części neutronów w warstwie.

- Dla warstw w pełni ukrytych [[hidden layer]], zwykle $0.5 - 0.8$ (więcej jak bliżej wyjścia)
- Dla warstw konwolucyjnych $0.1 - 0.2$ ([[CNN]] $\rightarrow$ [[ReLU]] $\rightarrow$ [[dropout]])
- Nie stosujemy na samym wyjściu
- **Wyłączamy po wytrenowaniu modelu**

*Pomaga uzyskać bardziej korzystny rozkład wag w sieci, wspomaga generalizację.*
#machineLearning #neuralNetwork 