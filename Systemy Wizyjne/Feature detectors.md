Detektory cech obrazowych, służą do wykrywania charakterystycznych cech na obrazie.

### Wykrywanie krawędzi na obrazie
- Gradient obrazu -- [[Sobel mask]] 
- Algorytm -- [[Canny algorithm]]

### Typowe detektory obrazowe
- W oparciu o funkcje autokorelacji -- [[Harris detector]]
- Szybki detektor -- [[FAST detector]]
- Skalowo-inwariantny -- [[SIFT detector]]
- SURF > SIFT (speed) -- [[SURF detector]]
- [[BRIEF detector]]
- ORB [[ORB detector]]
- 
### Deskryptory cech obrazowych [[feature descriptors]] 
W następnej kolejności, wykorzystuje się *deskryptory cech* do opisu cechy w oparciu o charakterystykę sąsiedztwa.

### Zastosowanie cech obrazowych
- Wyznaczanie przekształcenia (rotacji, translacji) pomiędzy dwoma obrazami z kamery ([[visual odometry]]).
- Sklejanie obrazów (panorama).
- Śledzenie obiektów ([[object tracking]]).
- Automatyczna nawigacja
- Rekonstrukcja 3D
- Rozpoznawanie miejsc
- Rozpoznawanie obiektów ([[object detection]])

### Problemy detekcji cech
- zmiana punktu widzenia (co może deformować obraz, zmieniając cechy)
- Zmiana jasności na obrazie
- Skalowanie obiektów
- Powtarzalność, względem punktu widzenia
- Złożoność obliczeniowa
#image_processing #feature_detection 