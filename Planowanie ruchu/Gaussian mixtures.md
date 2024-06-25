Mieszanina funkcji Gaussa:
$$
\displaystyle{
f(x_1, \dots, x_n) = \sum^m_{q=0}c_q \cdot e^{\left(\sum^n_{p=1} \lambda_{qp}(x_p - a_{qp})^2 \right)}}
$$
Współczynniki $c_q$ wyznaczamy za pomocą metody najmniejszych kwadratów:
$$
\mathbf{c} = (\mathbf{V}^T \cdot \mathbf{V})^{-1} \cdot \mathbf{V^T} \cdot \mathbf{r}
$$
gdzie:
$$
V = \begin{bmatrix}
\phi(p_{f_1}) && \phi_2(p_{f_1})) && \dots && \phi_m(p_{f_1}) \\
\vdots && \vdots &&\ddots && \vdots\\
\phi(p_{f_k}) && \phi_2(p_{f_k})) && \dots && \phi_m(p_{f_k} \\)
\end{bmatrix}
$$
jest macierzą Vandermonde'a, a $\mathbf{r}$ jest wektorem kolizji $f_c$ odpowiadającym punktom wejściowym $\mathbf{q}_r$.
wartości $\lambda_{qp}$ i $a_{qp}$ są uzywskiwane za pomocą metody [[PSO]].
### Przykłady
![[gaussian function approx.png]]
![[gaussian function approx 2.png]]
![[gaussian function approx 2D.png]]
![[gaussian modelling error.png]]

#robotics #motion_planning 
