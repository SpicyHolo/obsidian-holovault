Ograniczenia ruchu są brane pod uwagę podczas planowania ruchu robota ([[motion planning]]).

### [[2D motion constraints]]
### [[collision detection]]

### Inne ograniczenia ruchu
- [[robot workspace]]
- [[static stability]]
- [[dynamic stability]]

### Ograniczenia kinematyczne i kinodynamiczne
Ograniczenia dzielimy również ze względu na:
- kinematyczne (nieholonomiczne) 
- kinodynamiczne (na kinematykę, ale również na $v$ i $a$)
*W literaturze również pojawia się termin planowania trakejtorii, jest to pojęcie najbarzdziej ogólne i obejmuje ono oba powyższe przykłady, ale może również dotyczyć wyznaczenia sterowania $u(t)$*

### Ograniczenia kinematyczne
Wynikają ze struktury robota/agenta:
- rodzaj aktuatorów (liniowe / obrotowe)
- odległość pomiędzy przegubami
- maksymalne prędkości w przegubach
*Przykładem jest planowanie trajektorii robota manipulacyjnego (rozwiązywanie kinematyki prostej i odwrotnej, unikanie osobliwości i kolizji)*
### Ograniczenia kinodynamiczne
Dodatkowo obejmują:
- maksymalne przyspieszenia w przegubach
- ograniczenia na $M$, $F$
![[Pasted image 20240626012459.png]]