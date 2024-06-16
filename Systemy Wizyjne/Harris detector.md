**Detektor cech obrazowych, oparty o funkcje autokorelacji**.

- Analiza autokorelacji ([[autocorrelation]]) lokalnej funkcji obrazowej w 2D 
$$
A = \displaystyle{\sum_u\sum_vw(p,q) \cdot
\begin{bmatrix}
I_x^2  & I_xI_y \\
I_xI_y & I_y^2 \\
\end{bmatrix}
}
$$
*duże zmiany autokorelacji $\rightarrow$ obecność cechy*
- Funkcja punktująca (corner score)
$$
M_{c-H} = det(A) - \kappa \cdot trace^2(A)
$$
$$
M_{c-S-T} = \min(\lvert \lambda_1 \lvert, \lvert \lambda_2 \lvert)
$$
*Wartości funkcji punktującej będące **lokalnymi maksimami** i powyżej pewnej **wartości progowej** stają się **cechami***.

#image_processing #feature_detection 