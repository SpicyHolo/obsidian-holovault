- Klasyfikator wykorzystujący **las** drzew decyzyjnych ([[decision tree]]).
- Jest to tzw. klasyfikator zespołowy ([[ensemble classifier]]), które łączą wiele prostych klasyfikatorów, aby utworzyć jeden potężny.
- Ostateczny wynik klasyfikatora jest uzyskiwany w drodze głosowania.

![[random forest.jpg]]

### Uczenie lasu losowego
- Przy uczeniu każdego z drzew, wybierany jest pewien podzbiór cech (aby zapobiegać przeważaniu silnych cech)
- Dla $p$ cech, wielkość podzbioru jest ustalane zwykle na $p^{0.5}$

#machineLearning 