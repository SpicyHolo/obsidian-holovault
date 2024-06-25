#### punkt-sfera
$$
d = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2 + (z_1 - z_2)^2}
$$
warunek kolizji:
$$
d \leq r
$$
![[distance from circle.png]]
#### sfera-sfera
warunek kolizj:
$$
d \leq r_1 + r_2
$$
![[two circles distance.png]]
#### punkt - prostokąt
$$
^K\mathbf{p} = ^O\mathbf{K}^{-1} \cdot \;^O\mathbf{p}
$$
$$
^K\mathbf{p} = \begin{bmatrix}p_x && p_y && p_z && 1 \\ \end{bmatrix}^T
$$
warunek kolizji:
$$
\lvert p_x \lvert \leq a \land \lvert p_y \lvert \leq b
$$
![[rectangle distance.png]]

#### Axis-aligned Bounding Boxes ([[ABB]]) 
![[ABB.png]]

#### Object-oriented Bounding Boxes ([[OBB]]) 
![[OBB.png]]
#### Discrete Orientation Polytopes ([[k-DOPs]])
![[kDOPs.png]]

#robotics #motion_planning 