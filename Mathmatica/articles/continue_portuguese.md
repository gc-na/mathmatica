<!--
Meta Description: # Continue: Comando de Controle de Fluxo no Mathematica ## Sinopse O comando `Continue` em Mathematica é utilizado para controlar o fluxo de execução ...
Meta Keywords: continue, loop, mathematica, execução, iteração
-->

# Continue: Comando de Controle de Fluxo no Mathematica

## Sinopse
O comando `Continue` em Mathematica é utilizado para controlar o fluxo de execução dentro de estruturas de repetição, permitindo que a iteração atual seja interrompida e a próxima iteração seja iniciada imediatamente.

## Documentação
O `Continue` é um comando que pertence à categoria de controle de fluxo em Mathematica. Ele é especialmente útil dentro de loops como `For`, `While` e `Do`. Quando o `Continue` é chamado, a execução do loop é imediatamente transferida para a próxima iteração, ignorando qualquer código restante no corpo do loop para a iteração atual.

### Propósito
O propósito principal do `Continue` é proporcionar uma maneira de pular partes específicas de um loop com base em condições definidas, facilitando a filtragem de dados ou a execução de operações somente quando certas condições são atendidas.

### Uso
A sintaxe básica do `Continue` é:
```mathematica
Continue
```
Este comando deve ser utilizado dentro de um bloco de código que está sendo executado em um loop. Quando o `Continue` é alcançado, a execução do loop salta para a próxima iteração.

### Detalhes
- O `Continue` é frequentemente utilizado em conjunto com condicionais (`If`, `Which`, etc.) para determinar quando pular a iteração.
- O comando não retorna um valor; seu único propósito é controlar o fluxo do loop.

## Exemplos

### Exemplo 1: Uso Básico do Continue
```mathematica
For[i = 1, i <= 5, i++,
  If[Mod[i, 2] == 0, Continue[]];
  Print[i];
]
```
**Saída:**
```
1
3
5
```
Nesse exemplo, apenas os números ímpares de 1 a 5 são impressos, pois o `Continue` faz com que a execução pule a impressão dos números pares.

### Exemplo 2: Filtrando Valores em um Loop
```mathematica
Do[
  If[x < 0, Continue[]];
  Print[x^2];
  , {x, -2, 2}
]
```
**Saída:**
```
0
1
4
```
Aqui, os números negativos são ignorados, e apenas os quadrados dos números não negativos são impressos.

## Explicação
É importante notar que o `Continue` deve ser usado dentro de um loop; caso contrário, uma mensagem de erro será gerada. Outro ponto a ser considerado é a legibilidade do código: o uso excessivo do `Continue` pode tornar o fluxo de execução mais difícil de seguir, especialmente em loops complexos. Portanto, é aconselhável usá-lo com moderação e sempre com uma lógica clara.

## Resumo em Uma Linha
O `Continue` em Mathematica é um comando que permite pular a execução da iteração atual de um loop e prosseguir para a próxima.