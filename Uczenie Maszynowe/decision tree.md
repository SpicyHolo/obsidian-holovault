Podstawowy model klasyfikatora w uczeniu maszynowym [[Machine Learning]].

Gdzie każdy węzeł drzewa odpowiada przeprowadzeniu *testu na wartościach cech z próbki danych wejściowych.*

Są stosunkowe proste w interpretacji i implementacji i mało złożone obliczeniowo.

Ale mają stosunkowo niską dokładność (ale często jest wystarczająca).

![[decision tree.jpg]]

### Budowa drzewa decyzyjnego

- Chcemy na każdej gałęzi podzielić zbiór danych na jak najrówniejsze kawałki (najlepiej na pół).
- Najlepiej według cech, które są najbardziej istotne z punktu widzenia klasyfikacji.
- Zaczynamy od najbardziej ogólnych reguł.

### Algorytm ID3 

Wykorzystuje entropie([[enthropy]]) jako heurystyki wyboru atrybutu, który najlepiej dzieli zbiór.

Wybierane jest kryterium o największym zysku informacji (różnicy entriopi przed i po podziale).

![[decision tree boundaries.png]]
#machineLearning #classifier 
