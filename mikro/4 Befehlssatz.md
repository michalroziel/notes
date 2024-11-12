
# 4.1 Datenmanipulationsbefehle 

Die grün hinterlegden befehle sind vergleichsbefehle -> ändern nur die statusbits 
BLAU : keinen operand 1 
ROT : Klassisch logisch-arithmetischen befehle 

4 Bits : 16 BEfehle 
$rd : destination register 

sbz : should be zero
sbo : should be ones 

operand 2 kann register, immediate constante, shift sein 

#20 sbit : ...

#25 I bit : ...

## 4.1.1 Arithmetik- und Logikbefehle


```
Befehl{Bedingung}{S}      Rd,Rn, operand2
```


# -> # = Teppich 


# 4.1.2 Kopierbefehle 

MOv -> MOVE , MVN -> MOVE NOT 
	Hierbei können wir mit MVN auch -1 in ein Register reinladen 


# 4.1.3 Vergleichs- und Testbefehle 


# 4.1.4 Bit-Manipulationen 

Wir können bits setzten, löschen oder auch togglen 
Auch mehrere BIts auf einmal : Mit einer Bit Maske 


>[! Ein CMP auf 0 ist meistens nicht notwendig]


# 4.2 Multiplikationstabelle 


##### Prinzip der Kurzschlussauswertung
vergleiche skript seite 86 Beispiel #073
!! Wenn jemand verlangt, dass wir mehrere Sachen prüfen 


### Klausur  : kombinieren
zb : ladebefehl auch mit Modifiezierungsbefehl kombinieren können : nicht auswendig lernen 