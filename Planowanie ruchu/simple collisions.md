#### punkt-sfera
$$
d = \sqrt{(x_1 - x_2)^2 + (y_1 - y_2)^2 + (z_1 - z_2)^2}
$$
warunek kolizji:
$$
d \leq r
$$
![[Pasted image 20240623195412.png]]
#### sfera-sfera
warunek kolizj:
$$
d \leq r_1 + r_2
$$
![[Pasted image 20240623195550.png]]
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
![[Pasted image 20240623200308.png]]

#### Axis-aligned Bounding Boxes ([[ABB]]) 
![[Pasted image 20240623200614.png]]

#### Object-oriented Bounding Boxes ([[OBB]]) 
![[Pasted image 20240623200629.png]]
#### Discrete Orientation Polytopes ([[k-DOPs]])
![[Pasted image 20240623200636.png]]

#robotics #motion_planning 