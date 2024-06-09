Klasyfikator dla danych nadzorowanych.
W podstawowej wersji wykorzystuję *wektory (hiperpłaszczyzny)* do podziału przestrzeni na klasy.
W podstawowej wersji jest *klasyfikatorem binarnym.*

### Wady klasyfikatora

Przede wszystkim dane nie zawsze da się podzielić za pomocą funkcji liniowej:

![[svm_linear.png]]

### Kernel Trick

Przekształcenie danych wejściowych za pomocą nieliniowej funkcji, często zwiększającej wymiarowość danych.

![[data_2d_to_3d_hyperplane.png]]

### Nieliniowy SVM / Kernel SVM

Wykorzystanie innej funkcji do podziału danych:
- Wielomian
- RBF (radial basis function)
- Sigmoida
Większa złożoność klasyfikatora, wymaga więcej danych (ze względu na większą ilość parametrów)

### Wieloklasowy SVM

[[one vs all binary classifier]]


#machineLearning #classifier #supervisedLearning