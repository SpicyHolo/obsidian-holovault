Dla regularaotra **LQR** równanie opisujące macierz $S$ w sumie funkcji kosztu
$$
J^* = x^TSx
$$
Postaci:
$$
x^T(Q-SBR^{-1}B^TS + SA + A^TS)
$$
W bibliotekach do sterowania obiektami, rozwiązanie równania można znależć jako funkcje:
```python
S=CARE(A, B, Q, R)
```

#control #optimal_control 

