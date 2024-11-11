# Fang die Spionin

Ihr seid den Spioninnen immer weiter auf der Spur, ihr rechnet damit, dass ihr sie bald finden werdet!

... Aber was dann? Um für den Ernstfall gewappnet zu sein, wollt ihr üben, die Spioninnen zu fangen. 
Auch dabei kann euch zum Glück das Calliope Board helfen.

Dafür simuliert ihr auf dem Calliope folgende Situation: 
 
Ihr findet die Spionin, verfolgt sie zu Fuß und leitet sie in eine Sackgasse. 
Um euch zu entkommen, muss die Spionin also versuchen, irgendwie an euch vorbei zu laufen. 
Jetzt müsst ihr schnell reagieren können! Und genau das üben wir mit einem selbst programmierten Spiel auf dem Board.

Für diese Aufgabe werden wir viel mit den Blöcken aus dem **Spiel**-Block unter **Fortgeschritten** arbeiten. 
Klappt diesen also schon mal auf!

## Schritt 1: Start

Das Ganze werden wir auf der 5x5 Matrix und den beiden Knöpfen A und B aufbauen. 
Auf der Matrix werdet ihr durch eine leuchtende LED dargestellt, genauso wie auch die Spionin. 
Ihr versucht der Spionin den Weg zu blockieren, indem ihr euch in der untersten LED Reihe nach links und rechts bewegt, während die Spionin von oben geradewegs auf den Ausgang zuläuft.

Als allererstes erstellen wir zwei Variablen: 
Eine Variable *detektivin*, die euch darstellt, und eine *spionin* für eure Gegnerin. 
Diese Variablen werden im Verlauf des Spiels benutzt, um anzuzeigen, wo ihr euch bzw. die Spionin sich befindet.

Die beiden leuchtenden LEDs, die die Position von *detektivin* und *spionin* anzeigen, sind in diesem Spiel als sogenannte 'Sprites' eingestellt. 
Die zugehörigen Blöcke findet ihr in der Kategorie **Spiel**.

Beim Start platzieren wir uns erstmal selbst, also die LED für *detektivin*. 
Dafür brauchen wir den *erzeuge Sprite an Position x: y:*- Block aus **Spiel**. 
Dann kombinieren wir diesen mit *setze detektivin auf* aus dem **Variablen**-Block.
Beim Start vllen wir in der untersten Reihe in der Mitte stehen. 
Lege die x- und y-Koordinaten dementsprechend fest!

Außerdem setzen wir am Anfang unsere Anzahl an Leben auf 3, und den Spielstand auf 0. 
Beide Anweisungen dafür findest du wieder unter **Spiel**.

Als letztes setzen wir die drei RGB-Leuchten noch auf weiß.

## Schritt 2: Knöpfe programmieren

Jetzt schauen wir uns an, was passieren soll, wenn wir auf einem der Knöpfe unseres Calliope Boards drücken.
Diese sollen uns erlauben, uns nach links und rechts zu bewegen.

Da der Knopf A sich auf der linken und B sich auf der rechten Seite unseres Boards befinden, bewegt sich unsere *detektivin* nach links mit A und nach rechts mit B. 
Die Blöcke um die *detektivin* zu bewegen, findest du wieder unter **Spiel**.

Hier wirst du allerdings nicht die Anweisungen links oder rechts wiederfinden, sondern es wird mit Koordinaten gearbeitet. 
Dafür müssen wir wissen, dass wir uns in x-Richtung bewegen wollen, und ein Schritt immer eine Größe von 1 bzw. -1 hat.

Zusätzlich soll das Spiel beendet werden, wenn Knopf A und B gleichzeitig gedrückt werden.
Die Anzahl Leben wird auf 0 gesetzt.

## Schritt 3: Spielablauf

Alles was jetzt folgt, soll **dauerhaft** ablaufen.

Als allererstes setzen wir die RGB-Leuchten auf komplett weiß.
Dann wird die *spionin* auf die Matrix gesetzt:
Hierfür benutzen wir die gleichen Blöcke wie bereits oben bei der *detektivin*.

Anstatt der *spionin* jedoch einen festen Wert zuzuweisen, wollen wir den Überraschungseffekt simulieren - wir wissen schließlich nicht, welchen Weg die *spionin* wählen wird um an uns vorbei zu laufen!

Dafür brauchen wir den **Mathematik**-Block, um eine zufällige Zahl zwischen 0 und 4 zu erzeugen.
Diese Zahl wird als x-Koordinate der Spionin festgelegt.

Zwischen jedem Schritt pausiert die Spionin immer 500 ms.

Jetzt ist die *spionin* ganz oben auf der Matrix platziert.
Um bis uns herunter zu laufen muss sie 4-mal einen Schritt nach unten wiederholen.
Das machen wir ähnlich wie die links/rechts Bewegung unserer *detektivin*, nur dass wir unser y von *spionin* verändern.
Jeweils pausiert sie wieder 500 ms dazwischen.

## Schritt 4: Spionin gefangen?

Wir befinden uns immer noch im **dauerhaften** Spielablauf.

Wir wollen jetzt festlegen, was passiert **wenn** die Spionin gefangen wird.

Wir können kontrollieren, ob die *detektivin* der *spionin* in die Quere gekommen sind, indem wir als Bedingung für den wenn-dann-Block festlegen, ob die beiden sich berühren.

**Wenn** das der Fall ist, **dann**:
1. ändern wir den Spielstand um 1
2. löschen die *spionin*
3. zeigen grüne Lichter auf der RGB-Anzeige
4. pausieren 500 ms

**Ansonsten**:
1. entfernen wir 1 Leben
2. löschen die *spionin*
3. zeigen rote Lichter auf der RGB-Anzeige
4. pausieren 500 ms

Wenn ihr wollt, könnt ihr im **wenn-dann** und im **ansonsten** Block auch noch Soundeffekte einfügen, die zu der Situation 'Spionin gefangen' bzw. 'Spionin entkommen' passen!