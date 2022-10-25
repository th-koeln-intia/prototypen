# Prototyp Wäsche Melder

## Problem

Wäsche wird in der Waschmaschine vergessen, weil das Ende des Waschgangs nicht bemerkt wird.

## Lösung

Eine Waschmaschine, die weiß wann sie fertig ist und dann eine Benachrichtigung auslöst.

## Technische Lösung

Die Waschmaschine ist über einen smarten Zwischenstecker an den Strom angeschlossen. Dieser misst den Stromverbrauch der Waschmaschine und kann so Änderungen im Verbrauch erkennen. Wenn der Stromverbrauch unter einen Schwellenwert sinkt, ist das Waschprogramm der Waschmaschine fertig. Daraufhin wird eine Benachrichtigung ausgelöst.

![Image](analoger_prototyp.png?raw=true)

## Implementierung in Node-RED

Durch Beobachten der Waschmaschine werden Schwellenwerte ermittelt. Der gemessene Verbrauch der Maschine wird damit verglichen und bei einer Über- oder Unterschreitung dieser der Start oder der Stopp der Waschmaschine benachrichtigt.

![Image](node-red.png?raw=true)\
[Node-RED Flow](node-red.json)
