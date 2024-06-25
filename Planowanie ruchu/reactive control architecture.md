Działanie robota jest bezpośrednią reakcją na stan czujników, np. regulator PID:
• Zwierzęta często działają w ten sposób i są w stanie wytworzyć „inteligentne” działanie, np. mrówki
• Nie jest wymagana wiedza na temat całego otoczenia, wystarczy informacja o sąsiedztwie
• Pozwala na szybką reakcję na stan otoczenie (np. unikanie poślizgu)

![[reactive architecture.png]]
### Elementy architektury reakcyjnej:
• Refleks - szybka zakodowana reakcja na zdarzenie (odsunięcie ręki przy oparzeniu)
• Zachowanie behawioralne - reakcja zakodowana „w mięśniach” - np. jazda na rowerze
• Świadome zachowania - np. wytrenowane akrobacje

Właściwości:
• Szybka reakcja na nieprzewidziane zdarzenia
• Może być zaimplementowany w sprzęcie (elektronika,
mechanika)
• Niskie wymagania na moc obliczeniową
• Nawet proste reakcje mogą prowadzić do inteligentnego
zachowania (odkurzacz autonomiczny z prostym unikaniem
kolizji, robot BigDog)
• Może prowadzić do utknięcia w minimum lokalnym
(powtarzające się reakcje)

### Przykład - BostonDynamics' BigDog
![video](https://youtu.be/cNZPRsrwumQ)

Ale ma też swoje wady <3
![wady](https://youtu.be/oONc5NfvfKs)

### Architektura subsumpcyjna (Rodney Brooks)
![[subsumptic architecture.png]]
*Niezależne moduły ale tylko jedno sterowanie – wyjście z jednych*
*moduł zastępuje wyjście z innych modułów.* 

**Przykładowe warstwy:**
• Eksploruj środowisko
• Poruszaj się w losowym kierunku
• Unikaj kolizji z przeszkodami
*Pojawienie się przeszkody powoduje, że wyższe warstwy tracą*
*dostęp do aktuatorów.

### Architektura potencjałowa (Ronald Arkin, IJRR, 1987)
![[potential control architecture.png]]
*Niezależne moduły ale tylko jedno sterowanie – łączenie wyjść.*

**Przykładowe warstwy:**
• Unikaj przeszkód
• Idź do celu
• Idź do przodu
• Zostań na ścieżce

![[Pasted image 20240625191022.png]]
![[Pasted image 20240625191029.png]]

#robotics #motion_planning