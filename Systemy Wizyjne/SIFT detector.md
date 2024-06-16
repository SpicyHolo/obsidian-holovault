***S**cale-**I**nvariant **F**eature **T**ransform* 
### Odporność na przekształcenia
- Rotacja
- Zmiana oświetlenia
- Zmiana skali

## Deskryptor SIFT ([[SIFT descriptor]])

### Przestrzeń skali
- Filtrujemy obraz Gaussa o stopniowo rosnącym $\sigma$ ([[gauss filter]]), dokładniej o współczynnik $\sqrt{2}$ od poprzedniej wartości.
- Wyznaczamy różnicę sąsiadujących obrazów (ekwiwalent [[DoG]], [[blob detector]])
- Zmniejszamy obraz do połowy oryginalnego obrazu i powtarzamy poprzedni krok.

	![[scale space.png]]

	![[example_scale_space.png]]

### Tłumienie niemaksymalne w 3D
- Wykonujemy test odrzucania (podobny jak w detektorze Harrisa ([[Harris detector]])).
- Progowanie odrzuca słabe punkty kluczowe
### Interpolacja subpikselowa
- Do precyzyjnego lokalizowania punktów wykorzystane jest rozwinięcie *lokalnej funkcji [[DoG]]* w szereg Taylora ([[taylor series]])
$$
D(x) = D + \frac{\partial D^T}{\partial x}x + 
\frac{1}{2} x^T \frac{\partial^2D}{\partial x^2}x
$$
### Inwariancja na rotacje
- Wyznaczamy moduł i orientację gradientu dla każdego piksela w otoczeniu wykrytej cechy (kwadratowe okno, zgodne ze skalą wykrytej cechy).
$$
m(x, y) = \sqrt{\left 
(L(x + 1, y) - L^2(x-1,y) + \left[L(x, y + 1) - L(x, y - 1)\right]^2
\right)^2}
$$
$$
\theta(x, y) = \tan^{-1} \left(
\frac{L(x, y + 1) - L(x, y - 1)}{L(x+1, y) - L(x-1, y)}
\right)
$$
- Konstruujemy [[histogram]] orientacji gradientów ważonych modułami gradientów (36 kubełków).
- Najliczniej reprezentowana orientacja wybierana jest jako orientacja cechy.

### Deskryptor SIFT [[SIFT descriptor]]

#image_processing #feature_detection 