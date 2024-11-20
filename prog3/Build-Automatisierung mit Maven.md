
# Warum Maven ? 
Standardisierte Verwaltung von Java-Projekten, Auflösung von Abhängigkeiten und wiederholbare Prozesse für Software-Erstellung, -Test und -Bereitstellung.

## Make (Files)
Wir verwenden Makefür das Definieren von Build-Regeln 
Beschreibt Dependencies 

Bietet eine hohe Flexibilät und Modularität 
Ermöglicht selektive Kompilierung 

Weit verbreitet in Unix / Linux 

Einfacher Ansatz → steigende Komplexität

## Apache Ant 
Verwendung von .xml Dateien zur Definitionen von Build Prozessen 

Stärke : Plattformunabhängig in Java geschrieben 
Keine Festen Regeln 

Flexibilität → XML-Überlastung

## Apache Maven 
Im Vergleich zu Ant : einfachere Abhängigkeiten 
Automatisches Dependency Management 

Konvention vor Konfiguration → Standardisierung


Maven revolutioniert den Build-Prozess durch Konvention vor Konfiguration, automatisches Dependency Management und ein einheitliches Lifecycle-Modell.

POM.XML -> Project Object Management 

POM : beschreibt das WAS des Build-prozesses 

### Maven Build Lifecycles 
Maven folgt vordefinierten Build Lifeycles, die in verschiedene *Phasen* unterteitl sind 
Jede *Phase* hat ihre eigenen Goals, die erreicht werden müssen. 


### Vordefinierte Build Lifecycles 

**Default** : Der Hauptlebensyklus für den Build-Prozess, kann nicht direkt ausgeführt werden 
**Clean** : Bereinigt das Projekt, in dem zuvor erstellte Dateien gelöscht werden 
**Site** : Generiert Projekt Berichte und Dolkumentation 

Ausführen einer Phase -> alle vorhergehenden Phasen werden mit ausgeführt 
Ziele, welche einer *Phase* zugeordnet sind, werden automatisch ausgeführt. 

>[!Lebenszyklus : ]
>validate -> compile -> test -> package -> verify  -> install -> deploy 

validate:
	Überprüft die Vollständigkeit und Korrektheit des Programms 
compile:
	Kompiliert den QuellCode in Binärartefakte
test:
	Führt die deinierten Tests aus
package:
	Packt den kompilierten Code, z.B in eine JAR-Datei
verify:
	Überprüft die Gültigkeit des erstellten Pakets.
install:
	Installiert das Paket in das lokale Repository.
deploy:
	Überträgt das Paket in ein entferntes Repository.








