Klasyfikator złożony [[ensemble classifier]] wykorzystujący metodę **boost**, czyli szeregowe łączenie klasyfikatorów podrzędnych, wykorzystuję drzewa losowe (([[decision tree]]))

1. Uczymy proste drzewo decyzyjne tzw. (pieniek - stump)
2. Błędnym klasyfikacją przypisujemy większe wagi i uczymy kolejne drzewo, i tak w kółko
3. Tworzymy jeden duży klasyfikator, łącząc poszczególne klasyfikatory z odpowiednimi wagami

![[adaboost.png]]

### Rozpoznawanie twarzy ([[face detection]])
Przed sieciami neuronowymi *rozpoznawanie twarzy* było oparte na falkach Haara ([[haar wavelet]]) i algorytmie AdaBoost.
Rozpoznawał czy obiekt wewnątrz okna jest twarzą, zaczynając od prostych do bardziej złożonych cech.
