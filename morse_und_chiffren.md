# Geheime Botschaften :mag: :lock: <br>_Mission: Verschlüsselte Nachrichten_

St. Mary Mead, 2024:
Miss Marple ist schon seit einiger Zeit mit einem sehr heiklen Fall beschäftigt: Ein wertvoller technischer Prototyp wurde gestohlen und die Sicherheit des Landes steht auf dem Spiel. Da sie alleine nicht weitergekommen ist, hat sie euch um Hilfe gebeten.
Die ersten Beweise habt ihr bereits gefunden. Doch der Fall wird kompliziert, denn eine skrupellose Bande hört jeden eurer Schritte mit. In diesem brisanten Fall müssen alle Informationen sicher und geschickt verschlüsselt werden, damit sie nicht in die falschen Hände geraten. 

Die Aufgabe ist klar:
Eure Nachrichten an Miss Marple müssen so verschlüsselt werden, dass sie selbst in den Händen der Täter unverständlich bleiben.

Ihr entschließt euch dazu eure Aufgabe mit Hilfe der Calliope-Boards zu bewältigen...


<details>
<summary> Anforderungen </summary>

_Für dieses Projekt brauchen wir folgende Erweiterungen auf dem Calliope-Board:_
- `funk`
- `radio-broadcast`
</details>

## Kurze Einleitung: Was ist Morse? :black_circle::heavy_minus_sign::black_circle:

Morse ist eine Art von Schrift, die aus Punkten und Strichen besteht. Dabei steht jede Kombination von Punkt und Strich für ein bestimmtes Zeichen.

_Hier findest du die Liste der Morse-Codes zu Buchstaben, Zahlen und anderen Zeichen._
<details>
<summary> Lateinische Buchstaben </summary>

| Buchstabe | Morse-Code | Buchstabe | Morse-Code | Buchstabe | Morse-Code |
|-----------|------------|-----------|------------|-----------|------------|
| A         | `.-  `       | B         | `-...`       | C         | `-.-.`       |
| D         | `-.. `       | E         | `.   `       | F         | `..-.`       |
| G         | `--. `       | H         | `....`       | I         | `..  `       |
| J         | `.---`       | K         | `-.- `       | L         | `.-..`       |
| M         | `--  `       | N         | `-.  `       | O         | `--- `       |
| P         | `.--.`       | Q         | `--.-`       | R         | `.-. `       |
| S         | `... `       | T         | `-   `       | U         | `..- `       |
| V         | `...-`       | W         | `.-- `       | X         | `-..-`       |
| Y         | `-.--`       | Z         | `--..`       |           |            |

</details>

<details>
<summary> Zahlen </summary>

| Zahl | Morse-Code | Zahl | Morse-Code | Zahl | Morse-Code |
|------|------------|------|------------|------|------------|
| 0    | `-----`      | 1    | `.----`      | 2    | `..---`      |
| 3    | `...--`      | 4    | `....-`      | 5    | `.....`      |
| 6    | `-....`      | 7    | `--...`      | 8    | `---..`      |
| 9    | `----.`      |      |            |      |            |

</details>

<details>
<summary> Andere Zeichen </summary>

| Zeichen | Morse-Code | Zeichen | Morse-Code | Zeichen | Morse-Code |
|---------|------------|---------|------------|---------|------------|
| .       | `.-.-.-`     | ,       | `--..-- `    | ?       | `..--..`     |
| '       | `.----.`     | !       | `-.-.-- `    | /       | `-..-. `     |
| (       | `-.--. `     | )       | `-.--.- `    | &       | `.-... `     |
| :       | `---...`     | ;       | `-.-.-. `    | =       | `-...- `     |
| +       | `.-.-. `     | -       | `-....- `    | _       | `..--.-`     |
| "       | `.-..-.`     | $       | `...-..-`    | @       | `.--.-.`     |
| ¿       | `..-.- `     | ¡       | `--...- `    |         |            |

</details>

## Nachrichten senden :envelope:
<details>
<summary> Liste der Bausteine für diese Aufgabe </summary>

![beim Start](/_starcode_calliope_visuals//modules/grundlagen_beim_start.png)\
![LEDs](/_starcode_calliope_visuals//modules/grundlagen_zeige_led.png)\
![pausieren](/_starcode_calliope_visuals//modules/grundlagen_pausieren.png)\
![bildschirm Löschen](/_starcode_calliope_visuals//modules/grundlagen_bildschirm_loeschen.png)\
![Knopf](/_starcode_calliope_visuals//modules/eingabe_knopf.png)\
![Ton](/_starcode_calliope_visuals//modules/musik_spiele_note.png)\
![Funkgruppe](/_starcode_calliope_visuals//modules/funk_funkgruppe_setzen.png)\
![Sendeleistung](/_starcode_calliope_visuals//modules/funk_sendeleistung_setzen.png)\
![Zahl setzen](/_starcode_calliope_visuals//modules/funk_sende_zahl.png)

</details>
<br>

Um Nachrichten zu senden müssen wir **beim Start**..\
.. eine **Funkgruppe setzen**.\
.. die **Sendeleistung setzen**.

Die Funkgruppe kann beliebig gewählt werden, allerdings sollte sie auf beiden Geräten übereinstimmen.
Die Sendeleistung kann ebenfalls beliebig gewählt werden. Allerdings gilt:
 _Je höher die Zahl, desto weiter können die beiden Geräte voneinander entfernt sein._

:detective:_**Aufgabe:**_\
Setzt den folgenden Text im Calliope-Board um.

_Wenn_ **Knopf A geklickt** wurde, sollen die kurzen Signale über Funk gesendet werden.
Dafür wollen wir _erst_ die **Zahl 0** über Funk senden und anschließend dieses Muster auf den LEDs zeigen:\
![Kurzes Signal](/_starcode_calliope_visuals//kurz.png)\
Damit wir überprüfen können, ob unsere Eingabe auch wirklich geklappt hat, wollen wir unsere Eingabe mit einem **Ton hinterlegen**, der für **1/8 Schläge** hält.
Um nicht dauerhaft nur den Punkt auf den LEDs zu sehen, müssen wir ganz zum Schluss den Bildschriminhalt **löschen**.




_Wenn_ **Knopf B geklickt** wurde, sollen die langen Signale über Funk gesendet werden.
Dafür wollen wir hier _erst_ die **Zahl 1** über Funk senden und anschließend folgendes Muster auf den LEDs zeigen:\
![Langes Signal](/_starcode_calliope_visuals//lang.png)\
Auch hier wollen wir mit Hilfe eines Tons überprüfen, ob unsere Eingabe auch wirklich funktioniert hat. Dafür verwenden Wir einen **Ton**, der **1/4 Schläge** dauert. Ganz zum Schluss wird der das Muster auf dem Bildschirm **gelöscht**.

<details> 
<summary> Wichtige Information über Töne! </summary>

Damit Töne wahrgenommen werden können, müssen wir die Zeitdauer eines Tons festlegen.
Das machen wir mittels `pausiere ms("")`- Block. Mit diesem Block können wir die Anzeigedauer von Symbolen, Texten usw. einstellen. Die Länge des Tons lässt sich aus den Optionen beliebig wählen.\
Für uns ist wichtig, dass der **kurze Ton weniger ms** hat **als der lange Ton**.
</details>

## Nachrichten empfangen :incoming_envelope:

<details>
<summary> Liste der Bausteine für diese Aufgabe </summary>

![LEDs](/_starcode_calliope_visuals//modules/grundlagen_zeige_led.png)\
![pausieren](/_starcode_calliope_visuals//modules/grundlagen_pausieren.png)\
![bildschirm Löschen](/_starcode_calliope_visuals//modules/grundlagen_bildschirm_loeschen.png)\
![Wenn-Dann](/_starcode_calliope_visuals//modules/logik_wenn_dann.png)\
![Ton](/_starcode_calliope_visuals//modules/musik_spiele_note.png)\
![Datenpaket](/_starcode_calliope_visuals//modules/funk_datenpaket_empfangen.png)

</details>
<br>

:detective:_**Aufgabe:**_\
Setzt den folgenden Text im Calliope-Board um.

_Wenn_ wir ein **Datenpaket** über Funk **empfangen**, dann wird zwischen _2 Fällen_ unterschieden.
Entweder die erhaltene Zahl **entspricht der Zahl 0** oder die erhaltene Zahl **entspricht der Zahl 1**.

Für das Empfangen der **Zahl 0** sieht das Szenario wie folgt aus:
Auf den LEDs wir **das "kurze" Muster** angezeigt und es wird ein **Ton gespielt**, der **1/8 Schläge** hält. 
_(Bitte hier auch die **wichtige Information über Töne** beachten.)_
Anschließend wird der Inhalt des Bildschirms für weitere Zeichen wieder **gelöscht**.

Das Szenario für das Empfangen der **Zahl 1** verläuft nach dem selben Prinzip.

## Nachrichten verschlüsseln :lock_with_ink_pen:

Da Morse ein sehr weit verbreitetes System ist, ist es auch sehr einfach zu entschlüsseln. Jeder, der Zugriff auf die Tabellen hat, weiß, welche Informationen verschickt werden. Diese Tabellen sind öffentlich zugänglich.

Um die Täter also zu verwirren, wollen wir also ein neues System einführen, dass wie folgt aussieht:
Die **langen Sequenzen werden kurz** und die **kurzen Sequenzen werden lang**.
Dadurch entsteht eine _neue_ Morsetabelle, mit der ihr ungehindert informationen an Miss Marple weitergeben könnt.

:detective:_**Aufgabe:**_\
Verschickt einen Satz an Miss Marple und legt einen Zeit- und Treffpunkt zur Beweisübergabe fest.
> $Beispiel:$ "Treffpunkt heute Abend um 19:00 Uhr am alten Glockenturm."

<details>
<summary> Neue Morsetabellen </summary>

<details> 
<summary> Buchstaben </summary>

| Buchstabe | Original Morsecode | Vertauschter Morsecode | Neuer Buchstabe |
|-----------|--------------------|------------------------|----------|
| A         | `.-`               | `-.`                   | N        |
| B         | `-...`             | `.---`                 | J        |
| C         | `-.-.`             | `.-.-`                 | ع        |
| D         | `-..`              | `..-`                  | V        |
| E         | `.`                | `-`                    | T        |
| F         | `..-.`             | `--.-`                 | Q        |
| G         | `--.`              | `..-`                  | U        |
| H         | `....`             | `----`                 | Χ (griech.)        |
| I         | `..`               | `--`                   | M        |
| J         | `.---`             | `-...`                 | B        |
| K         | `-.-`              | `.-.`                  | R        |
| L         | `.-..`             | `.-..`                 | ל        |
| M         | `--`               | `..`                   | I        |
| N         | `-.`               | `.-`                   | A        |
| O         | `---`              | `...`                  | S        |
| P         | `.--.`             | `-..-`                 | X        |
| Q         | `--.-`             | `..-.`                 | F        |
| R         | `.-.`              | `-.-`                  | K        |
| S         | `...`              | `---`                  | O        |
| T         | `-`                | `.`                    | E        |
| U         | `..-`              | `--.`                  | G        |
| V         | `...-`             | `---.`                 | W        |
| W         | `.--`              | `-..`                  | D        |
| X         | `-..-`             | `.--.`                 | P        |
| Y         | `-.--`             | `.-..`                 | L        |
| Z         | `--..`             | `..--`                 | غ        |

</details>

<details> 
<summary> Zahlen </summary>

| Zahl | Original Morsecode | Vertauschter Morsecode | Neue Zahl |
|------|--------------------|------------------------|------|
| 0    | `-----`            | `.....`               | 5    |
| 1    | `.----`            | `-....`               | 6    |
| 2    | `..---`            | `--...`               | 7    |
| 3    | `...--`            | `---..`               | 8    |
| 4    | `....-`            | `----.`               | 9    |
| 5    | `.....`            | `-----`               | 0    |
| 6    | `-....`            | `.----`               | 1    |
| 7    | `--...`            | `..---`               | 2    |
| 8    | `---..`            | `...--`               | 3    |
| 9    | `----.`            | `....-`               | 4    |

</details>

<details> 
<summary> Andere Zeichen </summary>

| Zeichen | Original Morsecode | Vertauschter Morsecode | Neues Zeichen |
|---------|--------------------|------------------------|---------|
| .       | `.-.-.-`           | `-.-.-.`              | ;       |
| ,       | `--..--`           | `..--..`              | ?       |
| ?       | `..--..`           | `--..--`              | ,       |
| '       | `.----.`           | `-....-`              | -       |
| !       | `-.-.--`           | `.-.-..`              | 。      |
| /       | `-..-.`            | `.--.-`               | ー       |
| (       | `-.--.`            | `.-..-`               | ไ       |
| )       | `-.--.-`           | `.-..-.`              | "       |
| &       | `.-...`            | `-.---`               | ๆ       |
| :       | `---...`           | `...---`              |        |
| ;       | `-.-.-.`           | `.-.-.-`              | .       |
| =       | `-...-`            | `.---.`               | Ї       |
| +       | `.-.-.`            | `-.-.-`               | サ       |
| -       | `-....-`           | `.----.`              | '       |
| _       | `..--.-`           | `--..-.`              |        |
| "       | `.-..-.`           | `-.--.-`              | )       |
| $       | `...-..-`          | `---.--.`            |        |
| @       | `.--.-.`           | `-..-.-`               |        |
| ¿       | `..-.-`            | `--.-.`              | シ       |
| ¡       | `--...-`           | `..---.`              |        |
</details>


</details>

## Für Interessierte: Cäsars Code :speech_balloon:

Auch der große Cäsar hat damals Nachrichten verschlüsselt. Die weltweit bekannte **Cäsar Chiffre** verwendet ein System bei dem die Buchstaben im Alphabet **um 3 verschoben** werden. 
D.h. das A wird zu einem D, Das B zu einem E usw. Ist man am Ende des Alphabets angekommen (also bei "W wird zu Z"), fängt man **wieder am Anfang des Alphabets** an.

&rArr; _Falls ihr euch Fragt warum wir ausgerechnet um 3 verschieben:_
_Das liegt daran, dass Cäsar sich dachte, es sei eine hervoragende Idee den Anfangsbuchstaben seines Namens (C = der 3. Buchstabe im Alphabet) als Referenz zu nutzen. Natürlich ist das aber irgendwann aufgeflogen._

![Cäsar Cipher](/_starcode_calliope_visuals//Caesar-Chiffre.PNG)

:detective: Aufgabe:\
Versucht folgende Nachricht zu entschlüsseln.\
_(Hinweis: Sie enthält sowohl unsere Morse Verschlüsselung, als auch die Cäsar Chiffre)_

> FΧPΧ OSVΧFΧ;
> DGΧMMXF LΧGSΧBD VPM 5 PRG VF UΧG VSDΧF TלTSTKDRΧA。


<details>
<summary> Lösung! </summary>

<details>
<summary> Teil1: Code zurück in Morse umwandeln </summary>

> QHXH SODHQH.
> WUHIIHQ YHUOHJW DXI 0 XKU DQ GHU DOWHQ ELEOLRWKHN!
</details>


<details>
<summary> Teil2: Cäsar Chiffre entschlüsseln </summary>

> Neue Pläne.
> Treffen verlegt auf 0 Uhr an der alten Bibliothek!
</details>

</details>
