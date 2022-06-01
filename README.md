
# Rechnerarchitekturen Semester 4

# Inhaltsverzeichnis

- [Rechnerarchitekturen Semester 4](#rechnerarchitekturen-semester-4)
- [Inhaltsverzeichnis](#inhaltsverzeichnis)
  - [Klausurrelevante Kapitel](#klausurrelevante-kapitel)
    - [Kapitel 1.4 Röhren](#kapitel-14-röhren)
    - [Kapitel 2.2 Klassifizierung BS](#kapitel-22-klassifizierung-bs)
    - [Kapitel 2.2.1 Bitbreite](#kapitel-221-bitbreite)
    - [Kapitel 2.2.2 64-Bit-Verwechslung](#kapitel-222-64-bit-verwechslung)
    - [Kapitel 2.2.3 NX-Bit](#kapitel-223-nx-bit)
    - [Kapitel 2.3.4 CPU](#kapitel-234-cpu)
    - [Kapitel 2.3.6.2 Magnetisch](#kapitel-2362-magnetisch)
  - [Kapitel 2.4 Architekturen](#kapitel-24-architekturen)
  - [Kapitel 2.4.1 Von-Neumann](#kapitel-241-von-neumann)
  - [Kapitel 2.4.2](#kapitel-242)

## Klausurrelevante Kapitel

[1.4](#Kapitel1.4Röhren), [2.2](#Kapitel2.2KlassifizierungBS), [2.3.4](#Kapitel2.3.4CPU), 2.3.6.2, 2.4, 2.5, 3.3.1, 3.3.6 bis 3.3.10, 3.4.4,
5.2.2, 5.3, 5.4, 6.2.2, 6.2.8.4, 6.2.9.1, 7.2.1, 7.2.2, 7.3.3

---

### Kapitel 1.4 Röhren

Röhren: Versuch der 40er/50er Jahre, einen PC zu bauen. Bekanntes Modell der US Armee ENIAC, Verwendung von 18.000 Röhren mit einer gesamten Leistungsaufnahme von 174 kW. Jedoch unzuverlässig, da immer Röhren defekt.
GB funktionsfähige Maschine in WW2 mit 1500 Röhren, Leistungsaufnahme 4,5 kW

### Kapitel 2.2 Klassifizierung BS

### Kapitel 2.2.1 Bitbreite

Bitbreite wird durch die Menge des adressierbaren Speichers entschieden.
CPU könnte theoretisch mehr adressieren, jedoch EInschränkung durch Busbreite (z.B. 32 Bit).

Gängige Systeme auf dem Markt:

- 16 Bit (max. 64 Kilobyte RAM)
- 20 Bit (max 16 Bit + Segmentierung 1 MB)
- 32 Bit (max 4 GB)
- 64 Bit (max 64 ExaByte = 18 Millionen Terrabyte)

### Kapitel 2.2.2 64-Bit-Verwechslung

Jede Speicheradresse ist 64 Bit breit. Adressierung eines Datums dauert z.B. doppelt so lang gegenüber 32 Bit.
Vorteil ergibt sich erst, wenn mehr als 4 GB RAM verwendet werden.

Aktuelle Prozessoren verwenden zudem maximal 45 echte Adressleitungen, somit limitiert auf 45 Bit. Maximal anprechbarer Speicher sind damit 256 TB.

### Kapitel 2.2.3 NX-Bit

*No-eXecute-Bit*

Höchsten Bits einer 64 Bit Adresse selten verwendet. Deshalb Einführung von Sonderbefehle auf Bit 63 einiger Prozessorhersteller.

Verwendeung um zu speichern, ob an Adresse Daten oder Programmcode abgelegt ist. Dient dazu es zu erschweren, dass Schadcode in Speicher eingeschleust wird.

![64-Bit-Adresse](img/bs-44-bit.PNG)

### Kapitel 2.3.4 CPU

Die CPU (Central Processing Unit) ist zentrales Element in einem Computer. 

Mittlerweile in modernen PCs unter CPU noch kleinere Mikrocontroller, die z.B. aktiv sind, bevor eigentliche CPU gestartet ist.

CPU bedient alle Busse:

- Adressbus
- Datenbus
- Steuerbus

je nachdem, welche Aktionen benötigt werden.

![CPU Aufbau](img/cpu.PNG)

Interer Aufbau einer CPU normalerweise mit Registern dargestellt.

Bei alten CPUs immer bestimmtes Register bei arithmetischen oder logischen Funktionen involviert (=Akkumulator). Rechenergebnisse landen immer bei Akkumulator. Bei heutigen CPUs geschieht dies nur noch bei sspeziellen Befehlen.
Mittlerweile können mit jedem Register alle Operationen durchgeführt werden.

### Kapitel 2.3.6.2 Magnetisch
**Band**
Erste Massenspeicher waren Bänder. In Anfangszeit Zweckentfremdung von Audio-Tonspeichern.

Heutzutage immernoch bewährtes Medium zur Speicherung von Backups. 

Zugruff auf Bänder findet sequentiell statt.

- Nachteil: Zugriffsgeschwindigkeit gering, im Minutentbereich
- Vorteil: Bei Virenbefall nicht alle Daten direkt verfügbar: Verbreitung verlangsamt.

| Laufwerkstyp | Speichergröße |
| ------ | ------ |
|LTO-1 | 100 GB |
| ... | ... |
|LTO-8 | 12 TB |

**Diskette**

Zwischenlösung zwischen Magnetbandspeicher und Magnetplatte. Ähnlichkeiten mit Magnetband jedoch Vorteil des wahlfreien Zugriffs.

- Direkter Kontakt Schreiblesekopf und Medium
- starker Verschleiß und geringe Lebensdauer
- Entwicklung zu immer kleiner und höhrerer Speicherdichte

| Übliche Größe | Eingeführt | Speicher-Kapazität|
| --- | --- | --- |
| 8 Zoll | 1970er | 80 kByte bis 256 kByte |
| 5,25 Zoll | 1980er | 360 kByte bis 1,2 MByte |
| 3,5 Zoll | 1980er | 720 kByte bis 1,4 MByte |

**Platte**

Funktionsweise wie Bänder oder Disketten jedoch Schreiblesekopf schwebend über Medium. Der dadurch entstehende Luftwirbel der Rotation der Platte herrscht sorgt hierfür. Wenn Platte ausgeschaltet wird, fällt Kopf in eine Landing Zone, in der keine Daten gespeichert sind.

Vorteile:

- hohe Rotation und dadurch kurze Zugriffszeiten
- hohe Übertragungsrate

Hauptwartezeit hängt von Umdrehungsgeschwindigkeit ab, da Kopf im Mittel eine halbe Umdrehung warten muss, bis gesuchte Daten vorbei kommen.

Innenraum einer Festplatte ist mit staubfreiem Gas gefüllt. Staubpartikel würde zu Headcrash führen.

Speicherentwicklung kontinuierlich verbessert.

- Große Verbesserung durch GMR-Effekt (Giant Magneto Resistance): quantenmechanischer Effekt mit dem Zweck einen kleineren Lesekopf zu konstruieren. Ab 1995 konnte diese Technik in Platten genutzt werden.
- Weitere Steigerung 2008 durch Magnetisierung des Schreibkopfes
- 2013 SMR (Shingled Magnetic Recording) um mehr magnetische Bits auf eine Platte zu bekommen. Bei Magnetisierung eizelner Bits musste immer SIcherheitsabstand eingehalten werden. Schreibkopf ist größer als Lesekopf. Beim Lesen der nun kleineren Magnetzonen macht dies kein Problem, weil der wesentlich kleinere GMR-Lesekopf keine Probleme damit hat.

Aktuelle Festplatten speichern zwischen 2 Lücken aktuell ca. 40 MByte an Daten.

**Ausblick auf zukünftige Generationen**

Ausnutzung aller in der Vergangenheit eingeführten Technologien liefern maximale Größe von 18 TB.

- HAMR (Heat Assisted Magnetic Recording): Laser erhitzt zu schreibendes Material. Dadurch sinkt benötigte magnetische Feldstärke.
- MAMR (Microwave Assisted Magnetic Recording): direkt bei Schreibkopf Material aufgeweicht durch elektromagnetische Mikrowellenstrahlung.

## Kapitel 2.4 Architekturen

## Kapitel 2.4.1 Von-Neumann

Architektur, nach der fast alle modernen PCs aufgebaut sind. Erster Computer (Zuse Z1) hatte Von-Neumann Struktur.

Prinzip: es existiert nur ein einzelnes Bussystem. Dies können Daten oder Programmcode sein.

Nachteil: Bus wird abwechselnd für Speicher und Daten verwendet. Es wird nur eine Sorte Arbeitsspeicher benötigt, der für alles zuständig ist.

![Von-Neumann-Architektur](img/von-neumann.png)

Problem damals: Daten und Programmcode haben sich gegenseitig aus Cache "geworfen" (Cache-Trashing). Lösung durch Einführung von:

- Cache für Daten
- Cache für Programmcode

Vorgehen ähnelt CPU intern der [Harvard-Architektur](https://de.wikipedia.org/wiki/Harvard-Architektur)

**Nachteil der Von-Neumann Architketur:**

Software kann ihren eigenen Programmcode verändern. Schadsoftware kann dies als Möglichkeit der Ausbreitung nutzen.

## Kapitel 2.4.2

Entwicklung durch IBM und Harvard-Universität 1944.

**Wichtigstes Merkmal:**

Physikalisch getrennte Speicher und Busse für Programmcode und Daten.

![Harvard-Architektur](img/harvard.png)

Dadruch 2 Vorteile:

- Zugriff auf Speicher bei Befehlsabarbeitung doppelt so schnell
- Nahezu unmöglich, dass Programm eigenen Code überschreibt.

Programmspeicher ist bei normaler Ausführung Nur-Lese-Speicher. Bei Embedded Systemen oft sogar in ROM-Speicher abgelegt.

Modifizierte Version (Modified-Harvard) z.B. als Cache in modernen Systemen implementiert.