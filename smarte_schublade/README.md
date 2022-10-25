# Prototyp Smarte Schublade

## Problem

Eine Schublade wird zu häufig geöffnet, weil es nicht erkennbar ist, wie häufig dies tatsächlich geschieht.

## Lösung

Eine Schublade, die weiß, wie häufig sie geöffnet wird. Überschreitet die Anzahl der Öffnungen einen Schwellenwert, wird eine Lampe rot eingefärbt. Außerdem wird eine Statistik der Öffnungen über mehrere Tage angelegt.

## Einfache Technische Lösung

An der Schublade befindet sich ein Kontaktsensor. Dieser registriert Öffnungen und ermöglicht es diese zu zählen. Bei jeder Öffnung wird diese gezählt und in einen Graphen eingetragen. Wenn die Anzahl der Öffnungen einen Schwellenwert überschreitet, wird eine Lampe rot eingefärbt.

![Image](analoger_prototyp.png?raw=true)

### Einfache Implementierung in Node-RED

Die Anzahl der Öffnungen wird zu einem festgelegten Zeitpunkt zurückgesetzt.

![Image](node-red_einfach.png?raw=true)\
[Node-RED Flow](node-red_einfach.json)

## Komplexere Technische Lösung

Die Lampe soll wiederspiegeln wie häufig die Schublade geöffnet wurde. Dazu färbt sie sich langsam von grün zu rot.

![Image](analoger_prototyp.png?raw=true)

### Komplexe Implementierung in Node-RED

Die einfache Implementierung wird angepasst. Der Schwellenwert wird verwendet, um zu errechnen, wie sehr sich die Farbe bei jeder Öffnung ändert.

![Image](node-red_komplex.png?raw=true)\
[Node-RED Flow](node-red_komplex.json)