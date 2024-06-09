Klasyfikator w uczeniu nienadzorowanym, polegającym na podziale zbioru na **k** klastrów.

### Algorytm

1. Losowo wybieramy k-średnich wartości ze zbioru
2. Każdą próbkę przydzielamy do najbliższej średniej
3. Środek ciężkości każdej z grup staje się nową średnią
4. Algorytm jest powtarzany, aż do uzyskania zbieżności

Działa dobrze dla małej ilości klas, które są zrównoważone ([[unbalanced classes]])

#machineLearning #classifier #unsupervisedLearning
