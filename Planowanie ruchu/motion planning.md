W planowaniu ruchu możemy wyróżnić dwa podstawowe problemy - planowanie ścieżki, planowanie trajektorii.
### Planowanie ścieżki
*ścieżka, czyli inaczej sekwencja pozycji, w jakich ma znaleźć się robot*
$$
s = \left\{p_0, p_1, p_2, \dots, p_n \right\}
$$
#### Planowanie trajektorii
*sekwencja pozycji zależna od czasu*
$$
s_t = \left\{p_0(t), p_1(t), \dots, p_n(t)\right\}
$$
### Diagram kompletnego planowania ruchu
![[Pasted image 20240625160521.png]]
### Notacja Planowania ruchu
- Model świata $\mathbb{W}$
- Model robota (geometria i kinematyka). Konfiguracja oznaczona jako $\mathbf{q}$
- Przestrzeń konfiguracyjna $\mathbb{C}$, np. dla robota diff-drive
$$
\mathbb{C} = \left\{x, y, \Theta \right\} = \mathbb{R}^2 \times \mathbb{S}^1
$$
- Przestrzeń zajęta przez robota $\mathbb{A}(\mathbf{q})$
- Przestrzeń zajęta przez przeszkody $\mathbb{C}_{obst}$
- Wolna przestrzeń $\mathbb{C}_{free} = \mathbb{C} \setminus \mathbb{C}_{obst}$

 ![[motion planning notation diagram.png]]

*Powiększenie przeszkód o rozmiar robota, daje nam łatwiejsza planowanie ruchu dla modelu punktu materialnego*

### Planowanie ruchu w statycznym środowisku
- **Dekompozycja mapy do postaci grafu: [[map decomposition algs]]**
- **Algorytmy szukające ścieżki w grafie:  [[graph-based search algorithms]]**
- **Algorytmy próbkujące przestrzeń: [[sampling-based search algorithms]]**

### Planowanie ruchu z ograniczeniami kinodynamicznymi

### Planowanie w dynamicznym środowisku
- Wykorzystanie zwyczajnego algorytmu (np. A*, RRT, itp.), ale trzeba to zrobić szybko
- Planowanie ruchu w ograniczonym horyzoncie za pomocą znanych algorytmów (A*, RRT< itp.) *problem z minimami lokalnymi*.
- Wykorzystanie algorytmów dedykowanych ([[D-star]], [[Focused D-star]], [[Incremental A-star]], [[D-star lite]]).
### Open Motion Planning Library ([[OMPL]])

### Architektury sterowania [[control architecture]]




#robotics #motion_planning 