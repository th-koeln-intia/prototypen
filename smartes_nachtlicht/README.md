# Prototyp Smartes Nachtlicht

## Problem

Nachts ist es dunkel. Lichtschalter müssen im dunkeln gesucht werden, außerdem kann reguläres Licht Leute wecken.

## Lösung

Ein ausreichend dunkles Licht, welches automatisch angeht.

## Einfache Technische Lösung

Im Flur befindet sich ein Bewegungsmelder. Wenn dieser nachts ausgelöst wird, geht eine smarte Lampe an. Diese ist so eingestellt, dass sie möglichst niemanden aufweckt. Nur wenn die Sonne untergegangen ist, geht das Licht an. Geht die Sonne auf oder der Bewegungsmelder erkennt keine Bewegung mehr, wird die Lampe ausgeschaltet.

![Image](analoger_prototyp_einfach.png?raw=true)

### Einfache Implementierung in Node-RED

Ein Planer wird verwendet, um den Sonnenauf- und untergang zu erkennen.

![Image](node-red_einfach.png?raw=true) \
[Node-RED Flow](node-red_einfach.json)

## Komplexere Technische Lösung

Der Bewegungsmelder hat nur einen gewissen Radius, in welchem Bewegungen erkannt werden können. Deshalb soll auch das Öffnen einer Tür das Licht anschalten.

![Image](analoger_prototyp_komplex.png?raw=true)

### Komplexe Implementierung in Node-RED

Die einfache Implementierung wird angepasst, indem der Türkontakt eingefügt wird.

![Image](node-red_komplex.png?raw=true) \
[Node-RED Flow](node-red_komplex.json)