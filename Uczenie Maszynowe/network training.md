### Uczczenie sieci wielowarstwowych

Stosuje się algorytm: *[[backpropagation]]*, aby warstwa po warstwie aktualizować parametry sieci.

### Podział na epoki
Podział uczenia na Epoki [[epoch]] (epoka odpowiada podaniu na wejściu całego zbioru uczącego)

Definiuje się kryterium zatrzymania (np. dokładność / [[cost function]] na zbiorze walidacyjnym, nie polepszy się przez 10 epok)

### Stała uczenia
Wartość stałej uczenia można zmieniać wg harmonogramu, albo warunków.

### Normalizacja danych
Normalizacja danych: [[batchnorm]], [[dropout]], ogólnie poprawiają uzyskiwane wyniki i przyspieszają uczenie.

### Batch mode
W batch mode, podajemy cały zbiór uczący, ostateczne aktualizacja jest średnią z wkładu z poszczególnych próbek.

Dla bardzo dużych zbiorów danych: [[minibatch]], [[SGD]]