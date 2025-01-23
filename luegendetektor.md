# Lügendetektor
Glückwunsch, ihr habt eine der Spioninnen gefangen! Sie ist aber ganz schön hartnäckig und will euch nicht 
verraten, wo sie ihr Diebesgut versteckt hat. Ihr habt ein paar Vermutungen, aber woher wisst ihr,
welche die richtige ist? Ein Lügendetektor wäre jetzt praktisch...

Plötzlich fällt euch ein, dass ihr mit Calliope ja einfach selber einen Lügendetektor bauen könnt!
Also packt ihr euer Material aus und macht euch an die Arbeit.

### Schritt 1: Idee
Einen voll funktionsfähigen Lügendetektor können wir leider nicht bauen. Dafür sind die Sensoren
im Calliope Mini zu ungenau. Stattdessen können wir aber etwas simulieren, was einem echten Lügendetektor
schon sehr nahe kommt.

Der Calliope Mini hat nämlich Berührungssensoren, die andere Werte ausgeben, wenn ein Stromkreis geschlossen
wird. In unserem Fall berühren wir zwei Pins, einen Minus- und einen Pluspol. Wenn der Stromkreis
geschlossen ist kann unser Calliope messen, wie stark der Widerstand zwischen den zwei Polen ist.

<img src="_starcode_calliope_visuals/picture_touch_pins.png" width="349" height="322" class="center" style="display: block; margin-left: auto; margin-right: auto;"> <br>

In einem richtigen Lügendetektor würden wir jetzt jede Veränderung im elektrischen Widerstand der Haut
messen. Das Prinzip dahinter nennt sich [Elektrodermale Aktivität](https://de.wikipedia.org/wiki/Elektrodermale_Aktivit%C3%A4t).
Mit unseren Sensoren bekommen wir aber keine zuverlässigen Werte, deshalb schummeln wir ein bisschen:
Wir überprüfen nur, ob jemand die Pins anfasst, danach geben wir nach ein wenig Bedenkzeit eine zufällige
Antwort aus.

### Schritt 2: Code

Zuerst setzen den Pin P0 (also unseren Berührungssensor) auf den resistiven Berührungsmodus, damit er
so funktioniert wie oben beschrieben.

