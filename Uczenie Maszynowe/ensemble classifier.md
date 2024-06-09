Model klasyfikatora w uczeniu maszynowym, polegający na połączeniu kilku prostszych klasyfikatorów, najczęstszym tego typu algorytmem jest **[[random forest]].**

### Metody agregacji
*Czyli łączenia wyników poszczególnych klasyfikacji.*
- Głosowanie większościowe, lub z arbitralnym progiem
- Uśrednianie lub wyliczanie średniej ważonej (dla regresji)
- Kolejny algorytm (metapredyktor) specjalnie uczony do agregacji (stacking)

### Boosting

Polega na wykorzystaniu agregacji *szeregowej*, zamiast *równoległej.*
Zaczynając od predyktora z dużym obciążeniem, które redukowane jest za pomocą kolejnych predyktorów. Popularny jest algorytm [[adaBoost]]
### [[gradient boosting]]
Opisując nasz problem jako szukanie funkcji $f(x)$, która jak najlepiej dopasuje pary
$(x_1, y_1)$ do $(x_n, y_n)$. W praktyce, ograniczając się do pewnego podzbioru funkcji, możemy wykorzystać optymalizację gradientową.
$$\hat{y}={argmin}_{f(x)}L(y, f(x))$$
W podstawowej wersji:
1. Budujemy model z podzbioru danych.
2. Wykonujemy predykcję na całym zbiorze.
3. Wyznaczamy błąd predykcji i wyznaczamy nowy model na podstawie błędów obliczanych w poprzednim kroku za funkcję celu przyjmując minimalizację błędu (podobnie jak w [[neural network]]).
4. Predykcję nowego modelu są łączone z predykcją z kroku poprzedniego.
Iterujemy aż do uzyskania zbieżności, odpowiedniej wartości funkcji celu.

Popularne algorytmy **[[gradient boosting]]**:
- Dokładność - [[CatBoost]], [[XGBoost]]
- Szybkość - [[LightGBM]], [[CatBoost]]
- Domyślnie - [[CatBoost]]


#machineLearning #classifier