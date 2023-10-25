# Subnetzkonfiguration Aufgabe


Gegebenes Subnetz: 172.16.102.0/24

| Bereich                  | Hosts | Netzadresse | Subnetzmaske (Dezimal) |
|--------------------------|-----|-------------|------------------------|
| Abteilung 1              | 80  |             |                        |
| Abteilung 2              | 50  |             |                        |
| Abteilung 3              | 20  |             |                        |
| IT                       | 10  |             |                        |
| Restnetz falls vorhanden |     |             |                        |

## Ergebnis

| Bereich      | Hosts | Netzadresse     | Subnetzmaske (Dezimal) |
|--------------|-------|------------------|-------------------------|
| Abteilung 1  | 80    | 172.16.102.0     | 255.255.255.128         |
| Abteilung 2  | 50    | 172.16.102.128   | 255.255.255.192         |
| Abteilung 3  | 20    | 172.16.102.192   | 255.255.255.224         |
| IT           | 10    | 172.16.102.224   | 255.255.255.240         |
| Restnetz     | 15    | 172.16.102.240   | 255.255.255.255         |



## Erklärung

Um die Subnetzmaske zu finden, betrachten wir die Anzahl der Hostbits, die für jedes Subnetz reserviert sind. Für "Abteilung 1" gibt es 80 Hosts, was 2^7 (128) übersteigt, aber nicht 2^8 (256). Das bedeutet, wir benötigen 8 Bits für Hosts. In einer IPv4-Adresse gibt es insgesamt 32 Bits. Daher gibt es 32 - 8 = 24 Bits für das Netzwerk. Die Subnetzmaske für "Abteilung 1" lautet also 255.255.255.128, was den ersten 25 Bits (24 Netzwerkbits + 1 Bit für das Subnetz) festlegt.

- **Netzadresse für "Abteilung 2":** 172.16.102.128
- **Subnetzmaske für "Abteilung 2":** 255.255.255.192

  Für "Abteilung 2" gibt es 50 Hosts, was zwischen 2^6 (64) und 2^7 (128) liegt. Das bedeutet, wir benötigen 7 Bits für Hosts. Die ersten beiden Bits der letzten Oktett (128 und 64) sind festgelegt. Daher verwenden wir das dritte Bit, um das Subnetz zu definieren. Die Subnetzmaske ist 255.255.255.192 oder /26.

- **Netzadresse für "Abteilung 3":** 172.16.102.192
- **Subnetzmaske für "Abteilung 3":** 255.255.255.224

  Für "Abteilung 3" gibt es 20 Hosts, was 2^4 (16) übersteigt, aber nicht 2^5 (32). Wir benötigen 5 Bits für Hosts. Die ersten 3 Bits des letzten Oktetts (128, 64 und 32) sind festgelegt. Daher verwenden wir das vierte Bit, um das Subnetz zu definieren. Die Subnetzmaske ist 255.255.255.224 oder /28.

- **Netzadresse für "IT":** 172.16.102.224
- **Subnetzmaske für "IT":** 255.255.255.240

  Für "IT" gibt es 10 Hosts, was zwischen 2^3 (8) und 2^4 (16) liegt. Wir benötigen 4 Bits für Hosts. Die ersten 4 Bits des letzten Oktetts (128, 64, 32 und 16) sind festgelegt. Daher verwenden wir das fünfte Bit, um das Subnetz zu definieren. Die Subnetzmaske ist 255.255.255.240 oder /29.

- **Netzadresse für "Restnetz":** 172.16.102.240
- **Subnetzmaske für "Restnetz":** 255.255.255.240 oder /28

  Da für "Restnetz" 15 Hosts benötigt werden, verwenden wir 4 Bits für Hosts (2^4 = 16, aber die ersten und letzten Adressen sind reserviert). Die Subnetzmaske ist 255.255.255.240 oder /28.


## Wie man von der Subnetzmaske zur Netzadresse kommt

### Abteilung 1 (Subnetzmaske: 255.255.255.128 oder /25)

Angenommen, die Subnetzmaske ist 255.255.255.128 in binärer Form: 11111111.11111111.11111111.10000000. Die Netzadresse für Abteilung 1 ist 172.16.102.0.

### Abteilung 2 (Subnetzmaske: 255.255.255.192 oder /26)

Angenommen, die Subnetzmaske ist 255.255.255.192 in binärer Form: 11111111.11111111.11111111.11000000. Die Netzadresse für Abteilung 2 ist 172.16.102.192.

### Abteilung 3 (Subnetzmaske: 255.255.255.224 oder /27)

Angenommen, die Subnetzmaske ist 255.255.255.224 in binärer Form: 11111111.11111111.11111111.11100000. Die Netzadresse für Abteilung 3 ist 172.16.102.224.

### IT (Subnetzmaske: 255.255.255.240 oder /28)

Angenommen, die Subnetzmaske ist 255.255.255.240 in binärer Form: 11111111.11111111.11111111.11110000. Die Netzadresse für die IT-Abteilung ist 172.16.102.240.

### Restnetz (Subnetzmaske: 255.255.255.240 oder /28)

Angenommen, die Subnetzmaske ist 255.255.255.240 in binärer Form: 11111111.11111111.11111111.11110000. Die Netzadresse für das Restnetz ist 172.16.102.240.


