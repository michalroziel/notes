
- An welche Pins kann man externe Interrupts anschließen?
	- Mit PINSEL umschalten ergibt folgende Liste: 
		- EINT0 -> P0.1 | P0.16 
		- EINT1 -> P0.3 | P0.14
		- EINT2 -> P0.7 | P0.15 
		- EINT3 -> P0.9 | P0.20 | P0.30 

-  An welchem Register kann man einstellen, ob der Interrupt Pegelgesteuert oder flankengesteuert anschlagen soll?
-  		EXTMODE EXTPOLAR
-  Welche Register braucht man um Externe Iterrupts zu initialisieren?
- Wie viele Externe Interrupts kann man an den Mikroprozessor anschließen?
- 		4
- Mit welchem Register schaltet man die Pin-Funktionen um?
- Mit welchen Registern initialisiert man den Vector-Interrupt-Controller
- Wo im Code kann man ISRs hinschreiben?
-  Warum gibt es das Paritätsbit?
-  Wie viele Bits können die Datenworte des Mikroprozessors haben?
-  Welche Register benötigt man um den Timer zu initialisieren?
    
1. welche pins können als extint eingestellt werden? -> "einzelne pins auf port 0 und 1"
2. baudrate-formel
3. wieviele extints gibt es (4)
4. welche register für timer
5. welche register für UART
6. welche register für extint
7. welches register zum senden in UART (UxTHR)
8. welche arten von interrupts gibt es (spannungspegel mit LOW oder HIGH, flankenabhängig fallend oder steigend)
9. womit schaltet man die pin-funktionen um (PINSEL)

An welche Pins kann man externe Interrupts anschließen?

    EINT0: P0.1, P0.16
    EINT1: P0.3, P0.14
    EINT2: P0.7, P0.15
    EINT3: P0.9, P0.20, P0.30​

    .

An welchem Register kann man einstellen, ob der Interrupt pegelgesteuert oder flankengesteuert anschlagen soll?

    EXTMODE (flanken- oder pegelgesteuert)
    EXTPOLAR (steigende oder fallende Flanke bzw. High-/Low-Pegel)​

    .

Welche Register braucht man, um externe Interrupts zu initialisieren?

    PINSEL (zum Umschalten der Pin-Funktionen)
    EXTMODE (Flanken-/Pegelsteuerung)
    EXTPOLAR (Flankenrichtung/Pegel)
    EXTINT (zum Quittieren des Interrupts)
    VICIntEnable (um den Interrupt zu aktivieren)
    VICVectCntl & VICVectAddr (für die vektorisierte Interruptverarbeitung)​

    .

Wie viele externe Interrupts kann man an den Mikroprozessor anschließen?

    Vier (EINT0 bis EINT3)​

    .

Mit welchem Register schaltet man die Pin-Funktionen um?

    PINSEL0, PINSEL1, PINSEL2​

    .

Mit welchen Registern initialisiert man den Vektor-Interrupt-Controller (VIC)?

    VICIntEnable (Interrupt erlauben)
    VICIntSelect (IRQ oder FIQ wählen)
    VICVectCntlX (Priorität setzen)
    VICVectAddrX (ISR-Adresse setzen)​

    .

Wo im Code kann man ISRs hinschreiben?

    Interrupt-Service-Routinen (ISR) müssen als void ISR(void) __irq deklariert werden​

    .

Warum gibt es das Paritätsbit?

    Zur Fehlererkennung bei der seriellen Übertragung​

    .

Wie viele Bits können die Datenworte des Mikroprozessors haben?

    Der Prozessor arbeitet mit 32-Bit​

    .

Welche Register benötigt man, um den Timer zu initialisieren?

    TxPR (Prescaler)
    TxTCR (Start/Stop/Reset)
    TxMCR (Match-Funktion)
    TxMR0-TxMR3 (Match-Register)
    TxEMR (Match-Ausgabe)
    TxCCR (Capture-Steuerung)
    TxIR (Interrupt-Quittierung)​

        .

Zusätzliche Fragen aus deiner Liste:

    Baudrate-Formel:
        Frequenzteiler = P-Clock / (16 * Baudrate)
        Dann:
            UxDLL = Frequenzteiler % 256 (Low-Byte)
            UxDLM = Frequenzteiler / 256 (High-Byte)​

        .

Welche Register für UART?

    PINSEL0/PINSEL1 (Pin-Funktion)
    UxLCR (Datenbits, Stopbits, Parität)
    UxDLL, UxDLM (Baudrate)
    UxIER (Interrupts aktivieren)
    UxLSR (Status)
    UxTHR (Senden)
    UxRBR (Empfangen)
    UxFCR (FIFO-Steuerung)​

    .

Welche Register zum Senden in UART?

    UxTHR (Transmit Holding Register)​

    .

Welche Arten von Interrupts gibt es?

    Spannungspegelabhängig: LOW oder HIGH aktiv
    Flankenabhängig: Steigende oder fallende Flanke​

    .

Womit schaltet man die Pin-Funktionen um?

    PINSEL0, PINSEL1, PINSEL2
