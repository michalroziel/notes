

## Von Virtuellen zu physischen Speicher 

### Typisches Adressraum Layout 

Stack (Thread 0)
Stack (Thread 1)

Dynamisch Allokierte Daten (Heap)
statishc allokierte Daten
SHared Libraries
Instruktionenen / Code


Stack : Daten von Funktionsaufrufen : Parameter, lokale Variablen, Rücksprungadressen 
Heap : Dynamische Daten



## Der Speicher, zwei Prozesse 


## Hands on Erfahrung 

### Relocation Problem 

### Ziel : Separate Adressräume 

Variante 2 : 
Hardware + OS kümmern sich um Umrechnung im Hintegrund 


## Memory Management Uni - MMU 

- Verantwortlich für das Mapping von virtuellen auf physische Adressen 

### Page-Based Virtual Adressing 

- speicher eingeteilt in pages - 4KB 
- MMU liegt in CPU 
	- innerhalb einer page des OS liegen die Page Tables. MMU muss die BasisAdresse dieser PageTable wissen 
- ersten 20 Bits : Entscheiden welcher eintrag der Page Table der Relevante ist 
- Für jede Anwendung gibt es ihre eigene PageTable, und eine eigene Übersertzung 

- Jeder einzelner Prozess hat ie Illusion dasss es nur diesen gibt 
- Eine Übersetzung : Single Level 
	- Es gibt mehrere Stufen 

[NEXT TIME] : Page Tables, etc.  


## Page-Based Virtual Adressing 
- basierend auf einer Single-Level Page Table 

## Relocation Problem 

## Speicher für single-level Page Table

Page  Größe : 2^22 ? 


### Aufteilung in 4MB Stücke 

Ziel : Unbenutzte Page Tables nicht im Arbeitsspeicher zu referenzieren 

## Einführung eines Page Directory


[...]


### Virtual Address Translation 

Ziel : Anstatt einer 4MB Page Table : 4KB Page Table 


## Page Directory Entry (vereinfacht)

Jede Adresse : 32 Bit 
Entscheidung mit dem Present-Bit ob der Eintrag valide oder nicht ist 

Base Adresse von Page Table ist in Page Directory 
Base Adresse von Page Frame ist in Page Table


	Folie 99 : Zusammenfassender Vergleich 






