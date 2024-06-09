Inaczej nadmierne dopasowanie, a małe **własności uogólniające**.
- Błąd obciążenia (bias) - wynika z błędnych założeń w algorytmie, co sprawia, że nie wykrywamy istotnych związków między cechami, a wyjściem.
- Błąd wariancji (variance) - wynika z zbyt dużej czułości na małe zmiany w danych wejściowych, co powoduje dopasowanie do *losowego szumu* w danych wejściowych, a nie do *rzeczywistych reguł* w nich obecnych.

**Ważne jest osiągnięcie pewnego kompromisu.**

Przykład:

![[bias-variance-tradeoff.png]]

### Diagnozowanie błędów
- Bias - wysoki błąd na zbiorze uczącym i podobny błąd na zbiorze walidacyjnym.
- Variance - niski błąd na zbiorze uczącym, a wysoki na walidacyjnym.

### Radzenie sobie z kompromisem
#### Bias
-  Zdobycie większej ilości danych
-  Zmniejszenie ilości cech
-  Wybór innego modelu
#### Variance
-  Więcej iteracji algorytmu uczącego
-  Zwiększeni złożoności modelu
-  Dodanie większej liczby cech
-  Wybór innego modelu

#machineLearning #algorithmScore 