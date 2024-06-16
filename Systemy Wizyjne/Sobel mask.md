Maska służąca do wyznaczania gradientu obrazu, wykorzystywana w detektorach krawędzi:

$$
M_x =
\begin{bmatrix}
1 & 0 & -1 \\
2 & 0 & -2 \\
1 & 0 & -1 \\
\end{bmatrix},
M_y = 
\begin{bmatrix}
1 & 2 & 1 \\
0 & 0 & 0 \\
-1 & -2 & -1 \\
\end{bmatrix}
$$

### Moduł i kierunek gradientu
$$
M(x, y) = \sqrt{M_x(x, y)^2 + M_y(x, y)^2}
$$
$$
\theta(x, y) = \arctan \left( \displaystyle{\frac{M_y(x, y)}{M_x(x, y)}} \right)

$$
### Wizualizacja kierunku gradientu

![[image_gradient.png]]
#image_processing #feature_detection #calculus
