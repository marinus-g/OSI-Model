# OSI-Modell

## Schicht 1 (Bitübertragungsschicht, Physical Layer)

### LAN-Topologien:

#### Bustopologie:
- Alle PCs in einem Netzwerk sind mit einem fortlaufenden Kabel verbunden.
- Ein Paket wird an alle Netzwerkadapter in diesem Segment übertragen.
- Muss am Anfang und Ende terminiert werden.

#### Sterntopologie:
- Von jedem PC aus sind Kabelsegmente mit einer zentralen Komponente verbunden (z.B. Hub).

#### Ringtopologie:
- PCs sind über ein einziges ringförmiges Kabel verbunden.
- Ein "Token" kreist im Netzwerk, der Besitz des Tokens befähigt den PC, Daten zu senden.

#### Maschentopologie (Meshnetz – So ist das "Internet" (WAN) aufgebaut):
- Jeder PC ist mit jedem anderen PC durch ein separates Kabel verbunden.
- Vorteil: Ausfall eines Kabels bleibt ohne Folgen für die Stationen.

#### Hybride Topologie:
- Es werden zwei oder mehrere Topologien in einem Netzwerkentwurf kombiniert.

### Kabelarten:

#### Twisted Pair:
- Zwei miteinander verdrillte isolierte Kupferdrähte.
- Verhindert die Übertragung der Daten auf andere "Kabel".
    - Unshielded Twisted Pair (UTP)
    - Shielded Twisted Pair (STP)
    - Shielded Shielded Twisted Pair (SSTP)

#### Koaxialkabel:
- Eignen sich gut zum Überbrücken großer Entfernungen. (Wird, wenn dann, auf der letzten Meile genommen.)

#### Glasfaserkabel:
- Geeignet für Datenübertragung mit hoher Geschwindigkeit und Leistung.
- Übertragung über Licht.
- Unempfindlich gegenüber elektromagnetischen Wellen.

### IEEE 802 Standards:
- IEEE 802.3 – Ethernet
- IEEE 802.5 – Token Ring
- IEEE 802.8 – Glasfasermaterialien
- IEEE 802.11 – Wireless LAN

### Netzwerkkarte:
- Schicht 1 Verbindung, stellt Kommunikation zwischen Schicht 1 und 2 her.
- Empfangen von Daten und Umwandeln der Daten in elektrische Signale.
- Empfangen elektrischer Signale und Umwandeln in Daten.

## Schicht 2 (Data Link Layer - Sicherung)

Die Data Link Layer ist für die zuverlässige Übertragung von Daten zwischen direkt benachbarten Netzwerkelementen verantwortlich. Sie stellt sicher, dass die Daten fehlerfrei und in der richtigen Reihenfolge übertragen werden.

### Aufgaben der Data Link Layer:
- **Arbitration** Entscheidung
- **Rahmenbildung:** Teilt Daten in Frames für die Übertragung auf.
- **Adressierung:** Fügt physische oder MAC-Adressen hinzu, um Sender und Empfänger zu identifizieren.
- **Flusskontrolle:** Regelt den Datenfluss zwischen Sender und Empfänger.
- **Fehlererkennung und -korrektur:** Prüft auf Übertragungsfehler und korrigiert diese, falls möglich.
- **CarrierSenseMultipleAccessCollisionDetect** (GOOGLE)

- MAC Adresse
  - 48 Bit Adresse in Hex-Schreibweise
    - Die ersten 24Bit beschreiben den Hersteller
    - Die letzten 24 Bits werden vom Hersteller generiert

- Adressierungen
  - **Unicast-Adresse:**
    Eine Unicast-Adresse ist eine eindeutige Adresse für ein einzelnes Empfangsgerät in einem Netzwerk. Wenn Daten an eine Unicast-Adresse gesendet werden, werden sie nur von dem spezifischen Gerät empfangen, das diese Adresse besitzt. Zum Beispiel: Wenn du eine Webseite aufrufst, sendet dein Computer eine Unicast-Anforderung an den Server der Website, um die Daten zu erhalten.

  - **Broadcast-Adresse:**
    Eine Broadcast-Adresse wird verwendet, um Daten an alle Geräte in einem Netzwerksegment zu senden. Wenn Daten an eine Broadcast-Adresse gesendet werden, empfangen alle Geräte in diesem Netzwerksegment die Daten. Zum Beispiel: DHCP (Dynamic Host Configuration Protocol) verwendet Broadcast-Adressen, um IP-Adressen an Computer im Netzwerk zuzuweisen. Der DHCP-Server sendet eine Broadcast-Anfrage aus, und alle Computer im Netzwerksegment antworten. Nur derjenige, der die Anfrage beantwortet, erhält die IP-Adresse.

  - **Multicast-Adresse:**
    Eine Multicast-Adresse wird verwendet, um Daten an eine ausgewählte Gruppe von Geräten in einem Netzwerk zu senden. Geräte, die Mitglieder dieser Multicast-Gruppe sind, empfangen die Daten, während andere Geräte sie ignorieren. Zum Beispiel: Streaming von Videos über das Internet. Wenn mehrere Benutzer dasselbe Video ansehen, kann der Server die Daten als Multicast an eine spezifische Multicast-Adresse senden. Nur die Benutzer, die sich für diese Multicast-Gruppe angemeldet haben, empfangen die Videodaten.

  - **Berechnung von Netzwerkadressen:**
    - **Unicast-Adresse:** Eine Unicast-Adresse wird normalerweise von einem DHCP-Server zugewiesen oder manuell konfiguriert.

    - **Broadcast-Adresse:** Die Broadcast-Adresse in einem Netzwerk wird berechnet, indem alle Host-Bits in der IP-Adresse auf 1 gesetzt werden. Zum Beispiel, wenn eine IP-Adresse `192.168.1.0` mit Subnetzmaske `255.255.255.0` verwendet wird, ist die Broadcast-Adresse `192.168.1.255`.

    - **Multicast-Adresse:** Multicast-Adressen sind speziell im IPv4-Adressbereich reserviert. Sie reichen von `224.0.0.0` bis `239.255.255.255`.

- Fehlererkennung
  - 4 Bytes FCS (Frame Check Sequence)
  - Fehlererkennung, keine Fehlerkorrektur
  - ![](error-detection.png)



Die Data Link Layer bildet somit die Grundlage für die zuverlässige Übertragung von Daten in einem Netzwerk.


### Schicht 3
## Network Layer


## IP Adresse

Größe 32 Bits
Schreibweise ist Dezimal in 4 Oktetten
Aufteilung in 5 Klassen
Subnet Mask teilt IP Adresse in Netzwerkanteil und Hostanteil auf.
