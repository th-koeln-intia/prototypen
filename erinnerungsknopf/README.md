# Protoyp Erinnerungsknopf

## Problem

Wichtige Dinge werden vergessen, es ist aber nicht immer Zeit eine detaillierte Erinnerung einzurichten.

## Lösung

Eine Möglichkeit unaufwändig eine generelle Erinnerung zu stellen. Diese muss auch nebenbei nutzbar sein.

## Technische Lösung

Ein Knopf der gedrückt wird. Durch unterschiedliche Profile lassen sich unterschiedliche Zeiten einstellen. Wenn diese Zeit abläuft, wird eine Benachrichtigung ausgelöst.

![Image](analoger_prototyp.png?raw=true)

## Implementierung in Node-RED

Wenn der Knopf gedrückt wird, wird eine Erinnerung gestellt. Bei einfachem Drücken wird in einer Stunde erinnert, bei doppeltem in zwei. Wenn der Knopf gedrückt gehalten wird, wird die Zeit gemessen, bis dieser losgelassen wird. Diese Zeit wird dann in Minuten umgerechnet und dann in diesem Abstand erinnert. Die Erinnerung wird durch einen Delay realisiert.

![Image](node-red.png?raw=true)\
[Node-RED Flow](node-red.json)
