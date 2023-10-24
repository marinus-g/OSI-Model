# GTP OSI-Modell

## Schicht 1 (Bitübertragungsschicht, Physical Layer)

Die Bitübertragungsschicht ist für die Übertragung von Rohdatenbits über physische Medien verantwortlich. Sie bildet die Grundlage für die Übertragung von Daten in einem Netzwerk.

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
- **Arbitration:** Entscheidung
- **Rahmenbildung:** Teilt Daten in Frames für die Übertragung auf.
- **Adressierung:** Fügt physische oder MAC-Adressen hinzu, um Sender und Empfänger zu identifizieren.
- **Flusskontrolle:** Regelt den Datenfluss zwischen Sender und Empfänger.
- **Fehlererkennung und -korrektur:** Prüft auf Übertragungsfehler und korrigiert diese, falls möglich.

Die Data Link Layer bildet somit die Grundlage für die zuverlässige Übertragung von Daten in einem Netzwerk.

## Schicht 3 (Netzwerkschicht, Network Layer)

Die Netzwerkschicht ist für die Weiterleitung von Datenpaketen zwischen verschiedenen Netzwerken verantwortlich.

### Aufgaben der Netzwerkschicht:
- **Routing:** Bestimmt den besten Weg für Datenpakete zum Ziel.
- **Logische Adressierung:** Weist jedem Gerät im Netzwerk eine eindeutige IP-Adresse zu.
- **Paketvermittlung:** Teilt Daten in Pakete auf und leitet sie zum Ziel.

Die Netzwerkschicht ermöglicht die Kommunikation zwischen verschiedenen Netzwerken, indem sie den Datenverkehr zwischen ihnen steuert.

## Schicht 4 (Transportschicht, Transport Layer)

Die Transportschicht ist für die sichere und zuverlässige Übertragung von Daten zwischen Endgeräten verantwortlich.

### Aufgaben der Transportschicht:
- **Zuverlässige Datenübertragung:** Stellt sicher, dass Daten fehlerfrei und in der richtigen Reihenfolge übertragen werden.
- **Datenflusskontrolle:** Regelt den Datenfluss zwischen Sender und Empfänger.
- **Fehlererkennung und -korrektur:** Prüft auf Übertragungsfehler und korrigiert diese, falls möglich.

Die Transportschicht ermöglicht eine sichere End-to-End-Kommunikation zwischen Anwendungen auf verschiedenen Geräten im Netzwerk.

## Schicht 5 (Sitzungsschicht, Session Layer)

Die Sitzungsschicht ist für den Aufbau, die Aufrechterhaltung und die Beendigung von Sitzungen zwischen Anwendungen auf verschiedenen Geräten verantwortlich.

### Aufgaben der Sitzungsschicht:
- **Sitzungssteuerung:** Koordiniert den Datenaustausch zwischen Anwendungen.
- **Synchronisation:** Stellt sicher, dass Daten in der richtigen Reihenfolge übertragen werden.

Die Sitzungsschicht ermöglicht die Kommunikation und Koordination zwischen Anwendungen auf verschiedenen Geräten.

## Schicht 6 (Darstellungsschicht, Presentation Layer)

Die Darstellungsschicht ist für die Datenformatierung, Verschlüsselung und Kompression verantwortlich.

### Aufgaben der Darstellungsschicht:
- **Datenformatierung:** Wandelt Daten in ein für die Übertragung geeignetes Format um.
- **Verschlüsselung:** Schützt Daten vor unbefugtem Zugriff.
- **Kompression:** Reduziert die Größe von Daten für eine schnellere Übertragung.

Die Darstellungsschicht stellt sicher, dass Daten zwischen verschiedenen Systemen verständlich und sicher übertragen werden können.

## Schicht 7 (Anwendungsschicht, Application Layer)

Die Anwendungsschicht bietet Netzwerkdienste für Anwendungen und Endbenutzer.

### Aufgaben der Anwendungsschicht:
- **Bereitstellung von Diensten:** Stellt verschiedene Dienste wie E-Mail, Dateiübertragung und Webzugriff bereit.
- **Interaktion mit Anwendungen:** Ermöglicht die Kommunikation zwischen Anwendungen und dem Netzwerk.

Die Anwendungsschicht ermöglicht den Endbenutzern die Nutzung verschiedener Netzwerkdienste und Anwendungen.

---

**Hinweis:** Das OSI-Modell stellt sicher, dass verschiedene Netzwerkkomponenten miteinander kommunizieren können, unabhängig von ihrer Herkunft oder ihrem Zweck. Es dient als Grundlage für die Entwicklung und den Vergleich von Netzwerktechnologien und -protokollen.
