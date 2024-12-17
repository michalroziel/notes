
volatile keyword beschreiben können 
Vergleichsoperatoren kennen 

Wie Inhalt Register vertauschen ohne extra Register zu benutzen ? 

Programm Speicher :  Nur Lese Speicher 

align keyword 

PC- relative adressierung :
```
LDR R5,[PC,#offset]
```
DCD , DCW, DCB keywords 


Was ist das LR  - Link Register, und warum müssen wir es speichern ? 
Warum Speichern wir uns auf dem Stack die RücksprungAdresse ?
	Wenn wir vom unterprogramm ein neues unterprogramm aufrufen, vergessen wir nicht wohin wir am ende wieder springen müssen 

	
Was ist die ISR ? - Warum brauchen wir diese ? 

## Condition Flags mit und ohne Vorzeichen !


Flash : Geht von Adresse 0x00... bis hin zu 0x39....9 und ist ***READ ONLY*** 
Datenspeicher ist ***NICHT READ ONLY*** 
Was für ein Typ ist der Programmspeicher ? -> Flash Speicher 

```
RSB <Rd>, <Rn>, <Operand2>
Rd = Operand2 - Rn


REGULAR SUB : 
Rd = Rn - Operand2

```





# Versuch 1 

##  Ascii to unsigned int 

beliebige zahl von 0 bis 2^ 32 -1 


## Berechnung : 
Schauen  ob das 16 bit 0 oder 1 ist 
	wenn 1 dann zweierkomplement bilden 


