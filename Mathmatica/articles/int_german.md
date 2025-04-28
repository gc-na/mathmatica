<!--
Meta Description: # Mathematica: Die Funktion "int" – Integration in Mathematica ## Synopsis Die Funktion `int` in Mathematica ermöglicht die symbolische Integration vo...
Meta Keywords: die, mathematica, int, funktion, von
-->

# Mathematica: Die Funktion "int" – Integration in Mathematica

## Synopsis
Die Funktion `int` in Mathematica ermöglicht die symbolische Integration von mathematischen Ausdrücken. Sie ist essenziell für die Berechnung von Integralen, sowohl bestimmter als auch unbestimmter Art.

## Documentation
Die Funktion `int` wird in Mathematica verwendet, um Integrale zu berechnen. Der grundlegende Befehl hat die folgende Syntax:

```mathematica
int[f[x], x]
```

### Zweck
Die Hauptfunktion der `int`-Funktion besteht darin, die Fläche unter einer Kurve oder die Stammfunktion eines gegebenen Ausdrucks zu finden. Dies ist besonders nützlich in verschiedenen mathematischen und ingenieurtechnischen Anwendungen.

### Verwendung
- **Unbestimmtes Integral**: Um das unbestimmte Integral einer Funktion zu berechnen, verwenden Sie `int[f[x], x]`. Dies gibt die Stammfunktion von `f[x]` zurück.
  
- **Bestimmtes Integral**: Um das bestimmte Integral von `f[x]` über ein Intervall \([a, b]\) zu berechnen, wird die Syntax `int[f[x], {x, a, b}]` verwendet.

### Details
- Mathematica kann eine Vielzahl von Funktionen symbolisch integrieren, solange sie analytisch integrierbar sind.
- Bei Funktionen, die nicht analytisch integrierbar sind, gibt Mathematica möglicherweise eine numerische Approximation oder eine Meldung zurück.
- Die Funktion `int` ist besonders leistungsfähig in Kombination mit anderen Mathematica-Funktionen wie `Solve`, `Limit` und `Series`.

## Examples
Hier sind einige grundlegende Beispiele für die Verwendung der `int`-Funktion in Mathematica:

1. **Unbestimmtes Integral**:
   ```mathematica
   int[x^2, x]
   ```
   **Ergebnis**: \(\frac{x^3}{3} + C\)

2. **Bestimmtes Integral**:
   ```mathematica
   int[x^2, {x, 0, 1}]
   ```
   **Ergebnis**: \(\frac{1}{3}\)

3. **Komplexere Funktion**:
   ```mathematica
   int[Sin[x], x]
   ```
   **Ergebnis**: \(-\cos(x) + C\)

## Explanation
Bei der Verwendung der `int`-Funktion sollten einige häufige Stolpersteine beachtet werden:

- **Nicht alle Funktionen sind integrierbar**: Wenn Mathematica nicht in der Lage ist, ein Integral analytisch zu lösen, wird es Ihnen möglicherweise keine Lösung anbieten.
  
- **Integration von Variablen**: Achten Sie darauf, die Variable, nach der integriert wird, korrekt anzugeben, da dies zu falschen Ergebnissen führen kann.

- **Funktionale Unterschiede**: Beachten Sie, dass die Funktion `Integrate` in Mathematica die bevorzugte Methode für die symbolische Integration ist. Während `int` eine benutzerdefinierte Funktion darstellen kann, ist `Integrate` die standardmäßige und umfassendere Methode.

## One Line Summary
Die Funktion `int` in Mathematica ist ein leistungsfähiges Werkzeug zur symbolischen Integration von mathematischen Ausdrücken.