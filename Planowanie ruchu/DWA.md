Źródło[^1]
*Metoda lokalnego planowania ruchu robota*

#### Metoda pozwala na lokalne omijanie przeszkód:
• Bierze pod uwagę model kinematyczny robota
• Wykorzystywana jest mapa kosztów
• Testowane są lokalne trajektorie ruchu robota pod kątem przybliżenia do celu i unikania kolizji

![[DWA diagram.png]]
### Algorytm
• Próbkuj dopuszczalne sterowanie robota np. $\Delta x$, $\Delta \Theta$
 • Wygeneruj trajektorię robota dla zadanych wartości korzystając z modelu kinematyki robota
• Testowane są lokalne trajektorie ruchu robota pod kątem przybliżenia do celu i unikania kolizji
• Powtarzaj dla wszystkich dopuszczalnych sterowań i wybierz najlepszą trajektorię

>[!NOTE]
> Implementacja w ROS http://wiki.ros.org/dwa_local_planner

![video](https://youtu.be/0pigUC3L-VQ)
[^1]:Fox, D.; Burgard, W.; Thrun, S. (1997). ”The dynamic window approach to collision avoidance”. IEEE Robotics & Automation Magazine