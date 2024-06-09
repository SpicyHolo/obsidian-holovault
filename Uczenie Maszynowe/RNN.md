*Rekurencyjne sieci neuronowe,* umożliwiają generację ciągów (np. szeregów czasowych)
- Modelowanie rynku, finansów
- Analiza sygnałów czasowych [[time series analysis]]
- Przewidywanie zjawisk fizycznych

### Przetwarzanie mowy, tekstu

W przetwarzaniu tekstu w ostatnich latach korzysta się raczej z sieci typu [[transformer]].



![[rnn-1L.png]]![[RNN-ML.png]]

### Parametry sieci rekrencyjnej

- Wagi połączenia cech z warstwą ukrytą
- Wagi dla połączenia warstwy ukrytej z wyjśicem
- Wagi połączenia rekurencyjnego, dla połączenia z poprzednim krokiem czasowym

### Równania sieci

- Dla warstwy ukrytej:
$$\boldsymbol{z_h^{<t>}} = \boldsymbol{W}_{hx}\boldsymbol{x}^{<t>} + \boldsymbol{W}_{hh}\boldsymbol{h}^{<t-1>} + \boldsymbol{b}h$$
$$h^{<t>} = \sigma_h(\boldsymbol{z_h^{<t>}})$$
- Dla wyjścia:
$$\boldsymbol{z_y^{<t>}} = \boldsymbol{W}yh\boldsymbol{h}^{<t>} + \boldsymbol{b}y$$
$$\boldsymbol{y}^{<t>} = \sigma_y(\boldsymbol z_y^{<t>})$$
### Uczenie sieci rekurencyjnej

Wykorzystuje się algorytm *backpropagation through time*.
I polega na sumowaniu funkcji kosztu z kolejnych kroków w czasie.
Na wejście podajemy kompletną sekwencję w celu wyznaczenia funkcji kosztu, a później wykonujemy pełną wsteczną propagację wyznaczając gradienty
$$J = \sum^N_{t=1}J^{<t>}$$
**Problemy:** zanik i eksplozja gradientu, duża złożoność

W rozwiązaniu korzysta się z *truncated backpropagation through time*, gdzie dla wstecznej propagacji do wyznaczaniu gradientu wykorzystujemy tylko część ostatnich kroków.

### Sieci LSTM

[[LSTM]] to sieci z wbudowaną pamięcią.
modyfikację: GRU, RNN

### Filtry konwolucyjne 1-D
Do ekstrakcji cech, pełnią rolę filtru cyfrowego.

bazuje na nich:
[[ROCKET]] - RandOM Convolutional KErnel Transform

