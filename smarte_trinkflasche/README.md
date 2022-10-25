# Prototyp Smarte Trinkflasche

## Problem

Es wird vergessen Wasser zu trinken und deshalb zu wenig getrunken

## Lösung

Eine Wasserflasche, welche weiß wann aus ihr getrunken wird. Wenn zu lange nichts getrunken wird, wird erinnert.

## Einfache technische Lösung

An der Wasserflasche ist ein Erschütterungssensor, welcher erkennt, wenn die Flasche gekippt wird. Bei jedem Trinken wird diese gekippt und der Sensor schlägt aus. Wenn getrunken wird, wird ein Timer resettet und neu gestartet. Wenn dieser Timer abläuft, wird eine Benachrichtigung ausgelöst.

![Image](analoger_prototyp_einfach.png?raw=true)

### Implementierung in Node-RED

Wenn getrunken wird, wird der Zeitpunkt gespeichert und ein Timer gestartet. Wenn der Timer nun abläuft, wird mithilfe des gespeicherten Zeitpunkts überprüft, wie lange das letzte Trinken tatsächlich her ist. Falls während der Timer lief nicht noch ein mal getrunken wurde, wird eine Benachrichtigung ausgelöst.

![Image](node-red_einfach.png?raw=true)\
[Node-RED Flow](node-red_einfach.json)

## Komplexere technische Lösung

Zusätzlich zur einfachen Lösung wird gezählt wie häufig getrunken wurde. Bei jedem Trinken wird auch darüber benachrichtigt. Außerdem wird die Häufigkeit in einem Graph abgebildet. Der Zähler wird jeden Tag zu einer festgelegten Uhrzeit zurückgesetzt.

![Image](analoger_prototyp_komplex.png?raw=true)

### Implementierung in Node-RED

Die einfache Implementierung wird durch einen Zähler erweitert. Diese wird bei jedem Trinken erhöht und in einen Graph eingetragen.

![Image](node-red_komplex.png?raw=true)\
[Node-RED Flow](node-red_komplex.json)