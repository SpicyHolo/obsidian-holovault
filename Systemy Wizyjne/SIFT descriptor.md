*Deskryptor cech obrazowych dla metody **SIFT**.*
- Rozpatrujemy wycinek o rozmiarze $16 \times 16$ pikseli, którego środek jest cechą, wyznaczamy moduł i kierunek gradientu ([[Sobel mask]]).
- Dzielimy wycinek $16 \times 16$ na obszary $4 \times 4$ pod obszary i zbieramy 8-kubełkowy histogram orientacji dla każdego z nich.
- Ważymy histogramy pod obszarów funkcją Gaussa ze środkiem w środku opisywanego wycinka.
- Ostatecznie deskryptor składa się z $4 \times 4 \times 8 = 128 \text{ elementów}$.

bla bla nie chce mi się