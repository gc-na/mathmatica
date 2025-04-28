<!--
Meta Description: # int: Integración en Mathematica ## Sinopsis El comando `int` en Mathematica se utiliza para calcular integrales definidas e indefinidas de funciones...
Meta Keywords: mathematica, para, integrate, integrales, una
-->

# int: Integración en Mathematica

## Sinopsis
El comando `int` en Mathematica se utiliza para calcular integrales definidas e indefinidas de funciones matemáticas, permitiendo a los usuarios obtener resultados tanto simbólicos como numéricos.

## Documentación
El propósito del comando `int` es facilitar la integración de funciones, que es una operación fundamental en cálculo y análisis matemático. La función `Integrate` es la que se emplea en Mathematica para este propósito. Su uso principal puede dividirse en dos categorías: integrales indefinidas y definidas.

### Uso
1. **Integral Indefinida**: Se utiliza para encontrar la antiderivada de una función.
   ```mathematica
   Integrate[f[x], x]
   ```
   Donde `f[x]` es la función a integrar y `x` es la variable de integración.

2. **Integral Definida**: Se utiliza para calcular el área bajo la curva de una función en un intervalo específico `[a, b]`.
   ```mathematica
   Integrate[f[x], {x, a, b}]
   ```

### Detalles
- **Parámetros**:
  - `f[x]`: función a integrar.
  - `x`: variable de integración.
  - `a` y `b`: límites inferior y superior de la integral definida.
  
- **Salidas**:
  - Para integrales indefinidas, devuelve una expresión simbólica.
  - Para integrales definidas, devuelve un número o expresión que representa el área.

- **Opciones Adicionales**: Se pueden utilizar opciones adicionales para controlar el método de integración o para especificar condiciones, como `Assumptions`.

## Ejemplos
1. **Integral Indefinida**:
   ```mathematica
   Integrate[x^2, x]
   ```
   **Salida**: \(\frac{x^3}{3} + C\)

2. **Integral Definida**:
   ```mathematica
   Integrate[x^2, {x, 0, 1}]
   ```
   **Salida**: \(\frac{1}{3}\)

3. **Integral con Parámetros**:
   ```mathematica
   Integrate[a x^2, {x, 0, 1}]
   ```
   **Salida**: \(\frac{a}{3}\)

## Explicación
Al utilizar `Integrate`, es importante tener en cuenta que no todas las funciones pueden ser integradas de manera simbólica. Algunas integrales pueden no tener una solución cerrada, lo que podría llevar a Mathematica a devolver una respuesta en términos de funciones especiales o en forma numérica. 

### Errores Comunes
- Olvidar especificar los límites en integrales definidas puede llevar a resultados inesperados o implícitos.
- No usar las opciones adecuadas cuando se integran funciones con condiciones o parámetros puede resultar en errores o resultados incorrectos.

## Resumen en Una Línea
El comando `int` en Mathematica, a través de `Integrate`, permite calcular integrales simbólicas y numéricas de funciones matemáticas, facilitando el análisis y resolución de problemas en cálculo.