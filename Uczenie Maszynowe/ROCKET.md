
-  ROCKET przekształca szeregi czasowe za pomocą dużej liczby losowych konwolucji (dziesiątki tysięcy filtrów)
- Charakterystyki konwolucji wybierane są losowo (długości, wagi, bias, dylacja, padding)
- Przekształcone cechy są wykorzystywane do trenowania klasyfikatora liniowego


- Metoda ta jest bardzo szybka, a uzyskiwane wyniki często nie ustępują tym, które zwracają podejścia oparte o sieci neuronowe
- Jeszcze szybsza jest pochodna metoda MiniROCKET, zawierająca szereg usprawnień

- Dempster, A., Petitjean, F., & Webb, G. I. (2020). ROCKET: exceptionally fast and accurate time series classification using random convolutional kernels. _Data Mining and Knowledge Discovery_, _34_(5), 1454-1495.
- Dempster, A., Schmidt, D. F., & Webb, G. I. (2021, August). Minirocket: A very fast (almost) deterministic transform for time series classification. In Proceedings of the 27th ACM SIGKDD Conference on Knowledge Discovery & Data Mining (pp. 248-257).

![[1D convolution.png]]

#machineLearning #neuralNetwork 