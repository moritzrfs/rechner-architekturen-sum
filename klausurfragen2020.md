# Fecht Klausur Rechenarchitektur Juni 2020

### 1 in welchem Quartal wurde der erste nicht mechanische Computer gebaut 1234

1943 in Großbritannien zur Dechiffrierung geheimer Nachrichten

### 2 Ein 64 Bit Computer mit 3GBit RAM soll auf von einem 32 Bit System auf 64 Bit aufgerüstet werden, bringt das was für die Performance?

leicht sinken (Adressen werden bei 64Bit Systemen doppelt so lang wie bei 32 Bit  :arrow_right: Adressierung dauert länger)

### 3 Braucht man unbedingt ein 64 Bit System um ein 64 Bit Betriebssystem zu verwenden?

System Bit Breite: 
 
### 4 Warum sind die Adresseleitungen A0 A1 bei 32 Bit CPUs nicht notwendig

Da sich die Adressen bei 32-Bit-Datenbussen immer in 4 Byte schritten erhöhen und damit immer 3 Bytes übersprungen werden

### 5 Welche Entwicklung hat um die 2000er rum für eine Weiterentwicklung der magnetischen Festplatte gesorgt

Der GMR-Effekt (Giant Magneto Resistance): quantenmechanischer Effekt

### 6 Zeichnen sie das Schaltbild mit den Elementen (NICHT, ODER, UND) für einen Halbaddierer

### 7 RS485 wie wird erreicht, dass die Sender nicht gleichzeitig senden

Wegen Halbduplexverfahren kann jeder Sendeverstärker die Sendeverstärker der anderen Geräte abschalten

### 8 Wahlfreier Zugriff im Jahr 2020 DDR-DRAM wie schnell Zugriff?

Die Zugriffszeit bei DRAM-Speichern liegt heute bei ca. 40-60 nS

### 9 Welche Zelle für persisten Speicher gibt es nicht? [NAND,NOR, XOR, EEPROM]

XOR Speicher gibt es nicht

### 10 Softerror - wodurch wird er verursacht?

Durch kosmische Strahlung oder ionisierende Strahlung radioaktiver Isotope, die in Gehäuse gelangen kann, können einzelne Bits umkippen

### 11 Was folgt für serielle Netzwerke, wenn galvanische Trennung mit magnetischen Überträgern genutzt wird?

Lange Leitungen zur Übertragung möglich. Galvanisch = Elektronische Trennung zwischen 2 leifähigen Gegenständen. Bitmuster sind Gleichanteilsfrei

### 12 Welche Architektur hat mehrere Datenbusse?

Harvard Architektur: physikalisch getrennte Speicher und Busse für Programmcode und Daten

### 13 Warum wird eine neue digitale Schnittstelle bei Flachbildschirmen benötigt?

Neue Bildschirme nutzen digitale Signale. Mehrfache Digital-analog-Umwandlung gelingt nicht ohne Verluste

### 14 Was ändert sich bei USB 3.0 an der Übertragung?

Einführung 5 zusätzliche Leitungen als 2 differenzielle-fullduplex-Paare mit extra Massepin. Datenraten von bis zu 5 GBit/s.

### 15 Warum haben LCDs nur einen Wirkungsgrad von ca 16%?

50% werden bei der ersten Polfilter verloren. Anschließend Aufteilung in 3 Farben (RGB), bei denen jeweils nur 1/3 in die anzusteuernde Farbe fließt.

### 16 Was ist Sättingungsarithmetic/MMX?

Schnellere Signalverarbeitung. Addition nach Erreichen der Sättigung verhindern. Über/Unterlauf wierd verhindert. Ergebnis bleibt auf dem größt oder kleinsmöglichen Wert stehen.

### 17 Welcher Teil der CPU hilft bei einer FFT?

MAC

### 18 Was macht eine moderner Kompiler bei einer division mit 256 und welche vorteile bietet das?

Verschieben des SPeicherinhalts um eine Byte-Speicherstelle nach rechts

### 19 Was ist durch Pipelining möglich?

Deutliche Steigerung der Performance einer CPU