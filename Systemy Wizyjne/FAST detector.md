**F**eatures from **A**ccelerated **S**egment **T**est
- jeśli istnieje ciągły łuk przynajmniej $n$ pikseli jaśniejszych niż $I_p+t$ lub ciemniejszych niż $I_p -t$, piksel $p$ spełnia kryterium *testu segmentu*.
- Kolejność wykonywania testów jest ustalana przez algorytm uczenia maszynowego [[Machine Learning]] -- w wyniku powstaje drzewo decyzyjne [[decision tree]].

### Test segmentu
- Test segmentu zwraca skupiska kandydatów w pobliżu rzeczywistego położenia szukanej cechy
- Aby uzyskać dokładne współrzędne $(x, y)$, stosujemy *dodatkowe kryterium detekcji*.
### Funkcja punktująca
$$
V = \max 
\displaystyle{\left(
	\sum_{x\in S_{\text{bright}}} 
		\lvert I_{p \rightarrow x} - I_p \lvert - t,  
	\sum_{x\in S_{\text{dark}}}
		\lvert I_p - I_{p \rightarrow x} \lvert - t
\right )

}
$$

#image_processing #feature_detection 