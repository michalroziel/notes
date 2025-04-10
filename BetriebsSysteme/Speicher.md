

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


# Page-Bases Virtual Adressing Zeichnen können 


