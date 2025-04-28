<!--
Meta Description: # Die "While"-Schleife in Mathematica: Eine umfassende Anleitung ## Synopsis Die "While"-Schleife in Mathematica ist eine Kontrollstruktur, die es erm...
Meta Keywords: die, bedingung, ist, while, der
-->

# Die "While"-Schleife in Mathematica: Eine umfassende Anleitung

## Synopsis
Die "While"-Schleife in Mathematica ist eine Kontrollstruktur, die es ermöglicht, einen Codeblock wiederholt auszuführen, solange eine bestimmte Bedingung erfüllt ist. Diese Funktion ist besonders nützlich für iterative Berechnungen und Simulationen.

## Dokumentation
Die `While`-Anweisung hat die folgende Syntax:

```mathematica
While[bedingung, ausdruck]
```

### Zweck
Die `While`-Schleife wird verwendet, um einen Ausdruck solange zu wiederholen, bis die angegebene Bedingung `False` zurückgibt. Dies ist hilfreich in Situationen, in denen die Anzahl der Iterationen nicht im Voraus bekannt ist und von einer dynamischen Bedingung abhängt.

### Verwendung
1. **Bedingung**: Ein boolescher Ausdruck, der prüft, ob die Schleife fortgesetzt werden soll.
2. **Ausdruck**: Der Code, der ausgeführt wird, solange die Bedingung `True` ist.
   
Die Schleife wird so lange ausgeführt, bis die Bedingung `False` wird. Es ist wichtig, sicherzustellen, dass die Bedingung irgendwann `False` wird, um eine unendliche Schleife zu vermeiden.

### Details
- Die `While`-Schleife kann mit beliebigen Ausdrücken verwendet werden, die innerhalb der Schleife modifiziert werden können, um die Bedingung zu beeinflussen.
- Der Ausdruck wird sofort ausgeführt, sobald die Bedingung `True` ist, und es erfolgt eine erneute Überprüfung der Bedingung nach jedem Durchlauf.

## Beispiele

### Einfaches Beispiel
```mathematica
i = 1;
While[i <= 5, 
  Print[i]; 
  i++
]
```
In diesem Beispiel wird die Zahl `i` von 1 bis 5 ausgegeben.

### Verwendung mit einer Bedingung
```mathematica
sum = 0;
n = 1;
While[n <= 10,
  sum += n;
  n++
]
sum
```
Hier wird die Summe der ersten 10 natürlichen Zahlen berechnet.

### Komplexeres Beispiel
```mathematica
x = 1;
While[x < 100,
  x = x * 2;
]
x
```
In diesem Fall wird `x` verdoppelt, bis es 100 erreicht oder überschreitet.

## Erklärung
Ein häufiges Problem bei der Verwendung von `While`-Schleifen in Mathematica ist die Gefahr unendlicher Schleifen. Stellen Sie sicher, dass die Bedingung sich im Laufe der Iterationen ändert, um zu einem `False`-Ergebnis zu führen. 

Ein weiterer Punkt ist, dass die Ausdrücke innerhalb der Schleife sofort ausgeführt werden, was bedeutet, dass sie keine Rückgabewerte zurückgeben, es sei denn, sie sind explizit ausgegeben, wie in dem Beispiel mit `Print`.

## Ein-Satz-Zusammenfassung
Die `While`-Schleife in Mathematica ist eine leistungsstarke Möglichkeit, um wiederholte Berechnungen durchzuführen, solange eine bestimmte Bedingung erfüllt ist.