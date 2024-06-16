Algorytm do wyznaczania krawędzi na obrazie, sprawdza się lepiej niż czyste wyznaczanie gradientu obrazu, np. [[Sobel mask]].

### Poszczególne etapy algorytmu
1. Wstępne filtrowanie [[gauss filter]]
2. Dla każdego piksela w obrazie wyznaczamy gradienty w dwóch głównych kierunkach
3. Na podstawie gradientu wyznaczamy moduł i kierunek gradientu.
4. *Dla każdego punktu  sprawdzamy najbliższe dwa punkty sąsiadujące, leżące na kierunku obliczonego gradientu.*
5. *Jeśli rozpatrywany piksel ma maksimum funkcji obrazowej w tej trójce pikseli, piksel jest wygaszany w obrazie wynikowym, w przeciwnym razie jest pozostawiany.*
6. progowanie...
### Progowanie z histerezą
*Wykorzystuje wartości **TL** i **TH** do progowanie binarnego* [[binary thresholding]]
- Piksele powyżej wartości **TH** są zawsze pozostawiane.
- Piksele poniżej **TL** są zawsze wygaszane.
- Pomiędzy, są pozostawianie jeśli leżą na segmencie linii który łączy się z segmentem **TH**.
![[canny_th.png]]

### OpenCV2
```python
edges = cv2.Canny(img, tl, th)
```

#image_processing #feature_detection

