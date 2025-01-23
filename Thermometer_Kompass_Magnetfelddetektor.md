# Auf der Suche nach der Spionin!

Willkommen, Detektivinnen! Ihr habt bereits euren eigenen Detektivausweis erstellt und seid bereit für die nächste Mission. Ein geheimer Hinweis ist bei uns eingetroffen:

> „Die Spionin wurde zuletzt im Süden gesichtet. Die Temperatur an diesem Ort beträgt zwischen 18 und 26 Grad Celsius. Außerdem trägt er einen magnetischen Gegenstand bei sich!“

Eure Aufgabe: Findet die Spionin! Dafür verwandeln wir euer Calliope Board zuerst in ein Thermometer, um die Temperatur zu überprüfen. Dann in einen Kompass, um den Süden anzupeilen und danach in einen Magnetfelddetektor, um den verdächtigen Gegenstand zu finden. Los geht’s!

Aber bevor wir uns auf die Suche nach der Spionin machen, müssen wir erst noch unser Werkzeug kennenlernen, das wir dafür brauchen: Die **„Wenn… dann…“-Anweisung**! 

## Einführung: Wenn… dann… – Dein Werkzeug zum Überführen der Spionin!

Als Detektivin musst du wichtige Entscheidungen treffen, um Fälle zu lösen. Zum Beispiel: **„Wenn du Fußspuren siehst, folge ihnen.“** Genau so funktionieren Computer und damit auch dein Calliope, wenn sie programmiert werden! Sie können Entscheidungen treffen, basierend auf den Informationen, die sie erhalten. Das nennt man in der Programmierung eine **„Wenn… dann…“-Anweisung** oder „If-Statement“.

Eine **„Wenn… dann…“-Anweisung** sagt dem Computer:
1. **„Wenn etwas Bestimmtes passiert“** – z. B. „du findest Fußspuren“.
2. **„Dann mach folgendes“** – z. B. „folge ihnen“.

### Mehrere Entscheidungen gleichzeitig treffen

Aber was, wenn es keine Fußspuren gibt, sondern ein verdächtiger Hut am Boden liegt? Oder wenn weder Fußspuren noch ein Hut zu sehen sind? Hier kommen **„sonst wenn“ (else if)** und **„ansonsten“ (else)** ins Spiel! So kann ein Computer mehrere Bedingungen überprüfen und entsprechend handeln – wie eine Detektivin, die alle Möglichkeiten abwägt.

Ein Beispiel:
- **Wenn du Fußspuren siehst**, folge ihnen, um mehr Hinweise zu finden.
- **Sonst wenn ein Hut am Boden liegt**, untersuche ihn nach Fingerabdrücken.
- **Ansonsten**, schau dich genau um, ob du weitere Hinweise entdecken kannst.

Mit diesen Befehlen weiß der Computer (oder du als Detektivin!) genau, was zu tun ist, egal was passiert!

---

Mit diesen **Wenn… dann…-Anweisungen** kannst du deinem Computer oder deinem Calliope beibringen, kluge Entscheidungen zu treffen – genau wie eine clevere Detektivin! 
Und genau das brauchst du, um den Kompass und den Magnetfelddetektor zu programmieren, den wir in Schritt 2 und Schritt 3 gemeinsam bauen.
Aber zunächst starten wir erstmal mit einem Thermometer, bei dem noch keine **„Wenn… dann…“-Anweisung** gebraucht wird.


---

## Schritt 1: Das Calliope Board in ein Thermometer verwandeln

Der Zettel behauptet, dass die Temperatur am Ort der Spionin zwischen 18 und 26 Grad beträgt. Stimmt das? Finden wir es heraus, indem wir das Calliope in ein Thermometer verwandeln.
Wir möchten, dass das Calliope Board uns die ganze Zeit eine Zahl für die Temperatur anzeigt.

### Anleitung:

1. **Öffne die Programmierumgebung** für den Calliope mini.
2. **Erstelle ein neues Programm** und gebt ihm den Namen „Detektivinnen Thermometer“.

3. **Dauerhaft Block hinzufügen**
   - Gehe in die Kategorie **Grundlagen** und ziehe den Block **„Dauerhaft“** in den Arbeitsbereich.

4. **Zeige Zahl Block hinzufügen**
   - Wähle aus der Kategorie **Grundlagen** den Block **„zeige Zahl“** und ziehe ihn in den **„Dauerhaft“**-Block hinein.

5. **Temperatur in °C hinzufügen**
   - Gehe in die Kategorie **Eingabe** und wähle den Block **„Temperatur (°C)“** aus.
   - Ziehe den **„Temperatur (°C)“**-Block in das Feld hinter **„zeige Zahl“**.


6. **Spiele die Datei auf eurem Calliope Board ab**
   - Speichere die Datei und ziehe sie auf dein Calliope Board. Überprüfe, ob die Temperatur in eurer Umgebung eine Temperatur zwischen 18 und 26 Grad anzeigt. Passt das? Falls ja, seid ihr der Spionin
 schon dicht auf den Fersen!

---

## Schritt 2: Das Calliope Board in einen Kompass verwandeln

Um die Spionin zu finden, musst du zuerst die Himmelsrichtungen kennen! Der Kompass auf deinem Calliope hilft dir, den Süden anzusteuern. Wir wollen, dass uns die ganze Zeit Anfangsbuchstaben der Himmelsrichtungen (wie "S" für Süden) angezeigt werden. Dafür müssen wir davor die jeweiligen Bereiche der Gradzahlen in die Himmelsrichtungen übersetzen. 

## Anleitung

1. **Öffne die Programmierumgebung** für den Calliope mini.
2. **Erstelle ein neues Programm** und nenne es „Detektivinnen Kompass“.

4. **Dauerhaft Block hinzufügen**
   - Gehe in die Kategorie **Grundlagen** und ziehe den Block **„Dauerhaft“** in den Arbeitsbereich.

3. **Erstellt eine Variable für die Kompassausrichtung**:
   - Gehe in den Bereich **„Variablen“** und klicke auf **„Neue Variable erstellen“**.
   - Nenne die Variable `gradzahl`.
   - Ziehe aus der gleichen Kategorie den Block **„Setze gradzahl auf 0“** in den „Dauerhaft“-Block.
 
4. **Richtung in Grad ablesen**:
   - Gehe in die Kategorie **Eingabe** und zieh den Block **„Kompassausrichtung“** in das Feld neben **„Setze Gradzahl auf“**. So wird die aktuelle Richtung in der Variable `gradzahl` gespeichert.

5. **Logik für die Himmelsrichtungen hinzufügen**:
   - Gehe in die Kategorie **„Logik“** und zieh den Block **„Wenn wahr dann“** in den „Dauerhaft“-Block unter den roten Block.
   - Klicke auf das **Pluszeichen** im **„Wenn wahr dann“** Block, um eine weiteren „ansonsten“-Bedingungsblock hinzuzufügen. 
   - Klicke noch einmal auf das Plus unter dem ersten „ansonsten", um eine weitere Bedingung hinzuzufügen.
   - Klicke dann noch einmal auf das Plus unter dem nächsten „ansonsten", um eine weitere Bedingung hinzuzufügen.

6. **Himmelsrichtung Osten anzeigen**:
   - Gehe in die Kategorie **„Logik“** und ziehe den Block **„… und …“** in die erste dunkelgrüne Zeile in das Feld nach dem „wenn“.
   - Füge den Block **„0 < 0“** aus der Kategorie **„Logik“** vor das erste „und“ ein und ändert ihn auf **„gradzahl >= 46“** (die Variable gradzahl ist größer oder gleich 46).
   - Füge einen weiteren Block **„0 < 0“** nach dem „und“ ein und ändere ihn auf **„gradzahl < 135“** (die Variable gradzahl ist kleiner als 135).
   - Gehe in die Kategorie **„Grundlagen“** und füge den Block **„Zeige Text …“** in die erste weiße Zeile nach dem „dann“. Ändere den Text zu **„O“** für Osten. 
   Nun wird der Text "O" für Osten angezeigt, wenn eine Gradzahl zwischen 46 und 135 gemessen wird.

7. **Weitere Himmelsrichtungen hinzufügen**:
   - Gehe zum zweiten „Sonst wenn dann“-Bedingungsblock und füge dieselben Schritte wie oben hinzu, damit dort steht:  
     **„Sonst wenn gradzahl >= 135 und gradzahl < 225 dann zeige Text "S"“** (für Süden).
   - Wiederhole diesen Schritt für den nächsten „Sonst wenn“-Bedingungsblock, sodass dort steht:  
     **„Sonst wenn gradzahl >= 225 und gradzahl < 315 dann zeige Text "W"“** (für Westen).
   - Im letzten **„Ansonsten“**-Block soll der Text n mit dem Block **„Zeige Text N“** eingefügt werden, um die Himmelsrichtung Norden anzuzeigen, wenn keine der anderen Bedingungen erfüllt ist.

8. **Spiele die Datei auf eurem Calliope Board ab**
   - Speichere die Datei und ziehe sie auf dein Calliope Board.

9. **Kalibriere das Calliope mini**:
   - Bevor du das Programm abspielst, musst du das Calliope mini kalibrieren. Dabei siehst du Punkte auf dem Display. Dreht das Calliope, bis alle Punkte ausgefüllt sind. Wenn ihr das geschafft habt, seht ihr einen Smiley! Danach startet eurer Kompass.
   - Nun zeigt das Calliope mini die Himmelsrichtung basierend auf der Kompassausrichtung an.

9. **Süd-Richtung finden**:
   - Drehe das Calliope so, dass das "S" angezeigt wird. Jetzt schaust du genau nach Süden – in dieser Richtung wurde die Spionin zuletzt gesehen!

---

## Schritt 3: Das Calliope Board in einen Magnetfelddetektor verwandeln

Die Spionin trägt einen magnetischen Gegenstand bei sich – vielleicht etwas aus Metall, das magnetisch ist! Mit dem Magnetfelddetektor des Calliope könnt ihr überprüfen, ob magnetische Gegenstände in der Nähe sind. Wenn die Magnetfeldstärke hoch genug ist, sehr ihr einen Haken auf dem Calliope – das heißt, ihr habt etwas Verdächtiges gefunden!

### Anleitung:

1. **Dauerhaft Block hinzufügen**
   - Gehe in die Kategorie **Grundlagen** und ziehe den Block **„Dauerhaft“** in den Arbeitsbereich.

2. **Variable für Magnetkraft erstellen**:
   - Gehe in die Kategorie **„Variablen“** und klicke auf **„Neue Variable erstellen“**.
   - Nenne die Variable **`magnetkraft`**.
   - Wähle den Block **„Setze Magnetkraft auf 0“** aus der Kategorie **„Variablen“** und füge ihn in den Arbeitsbereich ein.

3. **Magnetkraft messen**:
   - Gehe in die Kategorie **„Eingaben“** und ziehe den Block **„Magnetfeldstärke (uT)“** in das Feld neben **„Setze Magnetkraft auf“**. Damit wird die aktuelle Magnetfeldstärke in Mikrotesla (uT) in der Variable `magnetkraft` gespeichert.

4. **Magnetfeldstärke überprüfen**:
   - Gehe in die Kategorie **„Logik“** und ziehe den Block **„Wenn wahr dann … ansonsten“** in den Arbeitsbereich.
   - Füge den Block **„0 < 0“** aus der Kategorie **„Logik“** in das Bedingungsfeld des **„Wenn … dann … ansonsten“**-Blocks ein.
   - Bearbeite den Block so, dass dort steht **„wenn magnetkraft < 90“**. Diese Bedingung überprüft, ob das Magnetfeld unter 90 Mikrotesla liegt.

5. **Symbole anzeigen**:
   - Gehe in die Kategorie **„Grundlagen“** und ziehte den Block **„Zeige Symbol“** in das weiße Feld nach dem "dann". 
   - Wähle das Symbol **„X“** als Anzeige, wenn die Magnetkraft unter 90 liegt.
   - Füge im nächsten weißen Feld nach dem „Ansonsten“ einen weiteren **„Zeige Symbol“**-Block ein und wähle das Symbol **„Haken“** als Anzeige, wenn die Magnetkraft 43 oder mehr beträgt.

6. **Spiele die Datei auf deinem Calliope Board ab**
   - Speichere die Datei und ziehe sie auf dein Calliope Board.

5. **Magnetfeld testen**:
   - Teste deinen Detektor, indem du das Calliope in der Nähe von magnetischen Gegenständen im Klassenzimmer hälst, z. B. am metallischen Tischbein oder der Heizung.
   - Zeigt das Calliope einen Haken an, hast du einen starken magnetischen Gegenstand gefunden; wenn es ein X anzeigt, ist der Gegenstand nicht magnetisch.
   
   ---

Jetzt bist du perfekt ausgerüstet, Detektivin! Mit deinem Kompass, Thermometer und Magnetfelddetektor kannst du der Spur der Spionin folgen und ihn aufspüren. Viel Erfolg bei der Mission!
