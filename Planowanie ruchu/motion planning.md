W planowaniu ruchu możemy wyróżnić dwa podstawowe problemy - planowanie ścieżki, planowanie trajektorii.
### Planowanie ścieżki
Czyli inaczej sekwencja pozycji, w jakich ma znaleźć się robot
$$
s = \left\{p_0, p_1, p_2, \dots, p_n \right\}
$$
#### Planowanie trajektorii
Jest to sekwencja pozycji zależna od czasu
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
- Przestrzeń zajęta przez