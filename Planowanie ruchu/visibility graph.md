Algorytm tworzący graf połączeń w mapie przeszkód dla robotów. 
Działa na zasadzie [[raytracing]].

![[visibility graph.png]]
>[!IMPORTANT]
> Metoda zwraca najkrótszą ścieżkę, ale bardzo blisko przeszkód.
> 
> ![[visibility graph path.png]]

> [!NOTE]
> Konstrukcja grafu widoczności może być czasochłonna $(n^2)$
> Lepsze wyniki przynosi tworzenie grafu widoczności w trakcie przeszukiwania[^1]
> 
> ![[visibility graph time complexity.png]]

[^1]: Marcell Missura, Daniel D. Lee, and Maren Bennewitz, Minimal Construct: Efficient Shortest Path Finding for Mobile Robots in Polygonal Maps, IROS, 2018




#robotics #motion_planning #graph #algorithm

