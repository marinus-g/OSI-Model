# Die Schichten des Osi Models (Selbst zusammengefasst)

### Schicht 1
### Bitübertragungsschicht | Physical Layer

## Lan Netzwerk
- **Local Area Network** Ist auf eine Locale Area begrenzt (z.B. Haushalt, Campus)
## Wan Netzwerk
- **Wide Area Network** Zusammenschluss von Lan Netzwerken, wird meistens vom Internetanbieter bereitgestellt 
    - Wird auch World Area Network teilweise genannt.
    - Es gibt auch Private WANs, welche von Unternehmen genutzt werden, um verschiedene Standorte privat zu Vernetzen.

## Lan Topographie
- **Bustopologie** Das gesamte LAN hängt an einem Kabel.
  - Wenn dieses Kabel einen Fehler aufweist, können Geräte nach diesem Fehler nicht mehr angesprochen werden.
    - Es ist also sehr Fehleranfällig
  - Kabel müssen am Ende terminated werden.

- **Sterntopologie** Das gesamte LAN hängt an einer zentralen Komponente (Hub).
  - Wenn ein Kabel ausfällt fällt nur das Gerät mit dem das Kabel verbunden ist aus.
  - Wenn der Hub ausfällt fallen jedoch alle Geräte aus.

- **Ringtopologie** Geräte sind über ein einzig Ringförmiges Kabel miteinander verbunden.
  - Daten werden in eine Richtung geschickt, entweder im Uhrzeigersinn oder gegen den Uhrzeigersinn.
  - Ein Gerät in einem Ringnetzwerk ist immer direkt mit zwei anderen Geräten verbunden. Dem vor und dem hinter ihm.
**Maschentopologie** Jedes Gerät ist mit jedem Gerät verbunden. Es gibt also eine direktverbindung zwischen jedem Gerät.
  - 
**Hybride Topologie** Es werden zwei oder mehr Topologien zusammengefasst.

## Kabelarten
**Twisted Pair**: Zwei Kupferkabel, welche zusammengedreht sind, um Interferenzen zu vermeiden.
  - Unshielded Twisted Pair (UTP)
  - Shielded Twisted Pair (STP)
  - Shielded Shielded Twisted Pair (SSTP)

**Koaxialkabel** Wird oft auf der letzten Meile verwendet. Waren damals Fernseh und Telefon Kabel

**Glasfaserkabel** Sendet Daten über Lichtwellen.
 - Hohe Übertragungsraten 
 - Unempfindlich gegenüber elektrischer Interferenzen
 - Empfindlich gegenüber physikalischer Eingriffe (abrupter Knick in der Leitung)

**IEE 802 Standards** Institute of Electrical and Electronics Engineers
  - *IEE 802.3* Ethernet
  - *IEE 802.5* Token Ring
  - *IEE 802.8* Glasfaser 
  - *IEE 802.11* WLAN (Wireless LAN - Wireless Local Area Network)

## NIC (Network Interface Card - Netzwerkkarte)
***Verbindung zwischen Schicht 1 und Schicht 2***
**Empfangen** von Daten und **umwandlung** in digitale Daten (Analog zu Digital)
**Umwandlung** digitaler Daten (elektrische Signale) (Digital zu Analog)

### Schicht 2
## Data Link Layer (Sicherung)
**Arbitration** Entscheidungen
**Rahmenbildung / Framing** Teilt die Daten in Frames für die Datenübertragung auf
**Adressierung** Fügt physische oder Mac-Adresse hinzu, um Sender oder Empfänger zu identifizieren
**Flusskontrolle** Regelt den Datenstrom zwischen Sender und Empfänger
**Fehlererkennung** Prüft auf Übertragungsfehler
**CarrierSenseMultipleAccessCollisionDetect**

***Mac Adresse***
  - **48 Bit Adresse in Hex**
  - **Die ersten 24** Bits dienen zur identifizierung des Herstellers
  - **Die letzten 24** Bits dienen zur identifizierung der Netzwerkkarte
  - **Die ersten 24** Bits werden vom Hersteller **gekauft**
  - **Die letzten 24** Bits werden vom Hersteller **generiert**

***Adressierungen***
  - **Unicast** Eindeutige Adresse für ein einzelnes Gerät in einem LAN
  - **Broadcast-Adresse** Die Broadcast-Adresse ist eine spezielle Netzwerkadresse, die dazu verwendet wird, Datenpakete an alle Geräte in einem Netzwerk zu senden.
    - In IPv4-Netzwerken wird die Broadcast-Adresse für das lokale Netzwerk durch das Setzen aller Host-Bits in der IP-Adresse auf 1 erstellt. 
  - **Multicast-Adresse** Wird verwendet, um an einzelne Gruppen Datenpakete zu schicken. Geräte müssen sich explizit für diese Gruppe anmelden.

**Fehlererkennung**
- **Checksummenprüfung**: Berechnung einer Prüfsumme für Datenpakete, die beim Empfänger überprüft wird.
- **CRC-Prüfung (Cyclic Redundancy Check)**: Verwendung eines speziellen Algorithmus zur Erkennung von Fehlern in Datenpaketen.
- **Paritätsprüfung**: Hinzufügen eines Paritätsbits zum Datenbyte, um Fehler zu erkennen.
- **Framing-Prüfung**: Überprüfung von Start- und Stopfbits sowie anderen Steuerzeichen in Datenrahmen zur Gewährleistung der Integrität.
