# Prototyp Kühlschrank Observer

## Problem

Die Tür vom Kühl- oder Gefrierschrank wird offengelassen.

## Lösung

 Die Tür des Geräts wird überwacht. Wenn sie jemand öffnet, wird nach einer festgelegten Zeit eine Benachrichtigung ausgelöst.

## Einfache technische Lösung

Die Tür des Kühl-/Gefrierschranks wird mit einem Türkontakt überwacht. Wenn die Tür geöffnet wird, wird ein Timer gestartet. Wenn dieser abläuft, wird erneut überprüft, ob die Tür geöffnet ist. Falls sie nicht geschlossen wurde, wird eine Benachrichtigung ausgelöst.

![Image](analoger_prototyp.png?raw=true)

### Einfache Implementierung in Node-RED

Wenn die Tür geöffnet wird, wird der Zeitpunkt gespeichert und ein Timer gestartet. Auch wenn die Tür geschlossen wird, wird der Zeitpunkt gespeichert. Wenn der Timer nun abläuft, werden diese beiden Zeitpunkte verglichen, um herauszufinden, ob die Tür tatsächlich eine Minute ununterbrochen geöffnet war. Falls ja, wird eine Benachrichtigung ausgelöst.

![Image](node-red_einfach.png?raw=true)\
[Node-RED Flow](node-red_einfach.json)

## Komplexere technische Lösung

Falls eine einfache Benachrichtigung nicht ausreicht, kann diese auch wiederholt werden. Hier wird alle 60 Sekunden erneut benachrichtigt. Nach fünf Benachrichtigungen, wenn die Türo also 5 Minuten offenstand, wird zusätzlich noch über ein anderes Medium benachrichtigt.

### Komplexere Implementierung in Node-RED

Die einfache Implementierung wird durch eine Schleife erweitert. Diese startet den Timer nach Ablauf neu. Die Durchläufe der Schleife werden gespeichert. Falls die Anzahl der Durchläufe einen festgelegten Schwellenwert überschreiten, wird eine Benachrichtigung ausgelöst.

![Image](node-red_komplex.png?raw=true)\
[Node-RED Flow](node-red_komplex.json)
