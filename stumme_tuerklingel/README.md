# Protoyp Stumme Türklingel

## Problem

Eine laute Klingel kann stören.

## Lösung

Die Klingel gibt kein akustisches Signal, sondern lässt eine Lampe blinken. Außerdem kann sie eine Benachrichtigung senden.

## Technische Lösung

Als Türklingel wird ein smarter Knopf verwendet. Wenn dieser gedrückt wird, blinkt eine Lampe. Um sicher zu gehen, dass das Blinken nicht übersehen wurde, wird an der Tür ein Kontaktsensor angebracht. Falls die Tür eine Minute nach dem klingeln nicht geöffnet wurde, wird zusätzlich benachrichtigt.

![Image](analoger_prototyp.png?raw=true)

## Implementierung in Node-RED

Wenn geklingelt wird, wird der Zeitpunkt gespeichert und ein Timer gestartet. Auch wenn die Tür geöffnet wird, wird der Zeitpunkt gespeichert. Wenn der Timer nun abläuft, werden diese beiden Zeitpunkte verglichen, um herauszufinden, ob die Tür schon geöffnet wurde. Falls nein wird eine Benachrichtigung ausgelöst.

![Image](node-red.png?raw=true)\
[Node-RED Flow](node-red.json)
