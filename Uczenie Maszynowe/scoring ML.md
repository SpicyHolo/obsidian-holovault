W przypadku klasyfikacji binarnej, mamy 4 klasy

![[ocena_algorytmu.jpg]]

#### Precyzja (precision)
Ile z *True* było poprawnych
$$precision = \frac{TP}{TP + FP}$$
#### Dokładność (accuracy)
Ile *True i False* trafionych ze wszystkich wyników
 $$accuracy = \frac{TP+TN}{TP + FP+TN+FN}$$
#### Czułość (recall)
Jak dobrze rozpoznaliśmy wszystkie *True*
$$recall = \frac{TP}{TP + FN}$$
#### F1 score
$$F = \frac{2\cdot precision \cdot recall}{precision + recall}$$
### Inne metody oceny, dla więcej niż 2 klas:
- [[confusion matrix]]
- [[ROC curve]]
- [[precision vs recall]]

Również błąd średnio kwadratowy, średni błąd bezwzględny dla regresji ([[regression]])

#machineLearning #algorithmScore 