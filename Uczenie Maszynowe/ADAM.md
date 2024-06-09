Adaptacyjnie dostosowuje wartość momentu spadku gradientu w optymalizacji.
- $\beta_1$, $\beta_2$ - stałe, $g_t$ - gradient w kroku t, $\varepsilon$ - niewielka stała (żeby nie dzielić przez zero)
$$
\begin{cases}
m_t = \beta_1m_t + (1 - \beta_1)g_t \\
v_t = \beta_2v_{t-1} + (1 - \beta_2)g_t^2 \\
\hat{m_t} = \displaystyle\frac{m_t}{1 - \beta_1^t} \\
\hat{v_t} \displaystyle\frac{v_t}{1 - \beta_2^t}
\end{cases}
$$
$$\theta_{t+1}=\theta_t - \displaystyle \frac{\eta}{\sqrt{\hat{v_t} + \varepsilon}}\hat{m_t}$$
**Najlepszy domyślny wybór (State of the art)**
More:
https://www.ruder.io/optimizing-gradient-descent/

#machineLearning #machineLearning #optimalisation
