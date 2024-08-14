---
author: Jean Branco
pubDatetime: 2024-08-10T21:00:40.000Z
modDatetime: 2024-08-10T21:00:40.000Z
title: Operadores Básicos de GoLang
slug: golangmini-operadores
featured: false
draft: false
tags:
 - golang
 - backend
 - minicurso
description: Conheça os Operadores Básicos e Essenciais da linguagem Go.
--- 


# GoLang MiniCurso - Aula 5: Operadores

Olá! Seja bem-vindo a mais uma aula do MiniCurso de GoLang! Nesta aula veremos sobre os Operadores em Go, pra que servem e como utiliza-los. Bora começar!?

## O que são Operadores?

Os Operadores, servem para realizar operações com expressões de variáveis e números. Nesta aula vamos falar sobre 4 deles, que são considerado essenciais para nossos programas. Veja um exemplo a seguir expressões que usam operadores.

```go
// O operador "=" é da classe de Operadores de Atribuição
var nome string = "Pedro"
```

```go
// O operador "+" é da classe de Operadores Aritméticos
fmt.Println(2 + 3) // Será imprimido apenas o resultado da operação
```

```go
var conta int = 5 * 5  // Operador "*" serve para realizar multiplicações
fmt.Println(conta) // 25 será imprimido na tela
```

> Isso foi apenas um gosto dos operadores, agora vamos ve-los de forma aprofundada.


### Operadores Aritméticos

Operadores aritméticos são usados ​​para realizar operações matemáticas comuns. Veja seguir a tabela de operadores aritméticos:

| Operador | Nome          | Descrição                                        |
|----------|---------------|--------------------------------------------------|
| +        | Adição        | Realiza a soma de valores                        |
| -        | Subtração     | Faz a subtração de valores                       |
| *        | Multiplicação | Multiplica valores                               |
| /        | Divisão       | Divide valores                                   |
| %        | Modulo        | Captura o RESTO da divisão de um valor por outro |

Veja os exemplos a seguir:

```go
a := 5
b := 3
resultado := a + b
fmt.Println("Resultado:", resultado)

// Saída: Resultado: 8
```

```go
a := 5
b := 3
resultado := a - b
fmt.Println("Resultado:", resultado)

// Saída: Resultado: 2
```

```go
a := 5
b := 3
resultado := a * b
fmt.Println("Resultado:", resultado)

// Saída: Resultado: 15
```

```go
a := 5
b := 3
resultado := a / b
fmt.Println("Resultado:", resultado)

// Saída: Resultado: 1
```

```go
a := 5
b := 3
resultado := a % b
fmt.Println("Resultado:", resultado)

// Saída: Resultado: 2
```

### Operadores de Atribuição

Os operadores de atribuição são usados para atribuir valores a variáveis e, em alguns casos, realizar operações ao mesmo tempo. Veja a tabela abaixo para entender melhor cada operador:

| Operador | Nome                         | Descrição                                            |
|----------|------------------------------|------------------------------------------------------|
| =        | Atribuição simples           | Atribui um valor a uma variável                      |
| +=       | Atribuição com soma          | Adiciona o valor à variável e atribui o resultado    |
| -=       | Atribuição com subtração     | Subtrai o valor da variável e atribui o resultado    |
| *=       | Atribuição com multiplicação | Multiplica o valor da variável e atribui o resultado |
| /=       | Atribuição com divisão       | Divide o valor da variável e atribui o resultado     |
| %=       | Atribuição com módulo        | Calcula o módulo e atribui o resultado               |

Veja os exemplos a seguir:

```go
a := 5
a = 10
fmt.Println(a) // Saída: 10
```

```go
a := 5
a += 3
fmt.Println(a) // Saída: 8
```

```go
a := 5
a -= 3
fmt.Println(a) // Saída: 2
```

```go
a := 5
a *= 3
fmt.Println(a) // Saída: 15
```

```go
a := 5
a /= 3
fmt.Println(a) // Saída: 1
```

```go
a := 5
a %= 3
fmt.Println(a) // Saída: 2
```

### Operadores de Comparação

Os operadores de comparação são usados para comparar valores e retornar um valor booleano (true ou false). Veja a tabela abaixo para entender melhor cada operador:

| Operador | Nome           | Descrição                                                                  |
|----------|----------------|----------------------------------------------------------------------------|
| ==       | Igual          | Retorna verdadeiro se os valores forem iguais                              |
| !=       | Diferente      | Retorna verdadeiro se os valores forem diferentes                          |
| >        | Maior que      | Retorna verdadeiro se o valor da esquerda for maior que o da direita       |
| <        | Menor que      | Retorna verdadeiro se o valor da esquerda for menor que o da direita       |
| >=       | Maior ou igual | Retorna verdadeiro se o valor da esquerda for maior ou igual ao da direita |
| <=       | Menor ou igual | Retorna verdadeiro se o valor da esquerda for menor ou igual ao da direita |

Exemplos:

```go
a := 5
b := 3
fmt.Println(a == b) // Saída: false
```

```go
a := 5
b := 3
fmt.Println(a != b) // Saída: true
```

```go
a := 5
b := 3
fmt.Println(a > b) // Saída: true
```

```go
a := 5
b := 3
fmt.Println(a < b) // Saída: false
```

```go
a := 5
b := 3
fmt.Println(a >= b) // Saída: true
```

```go
a := 5
b := 3
fmt.Println(a <= b) // Saída: false
```

### Operadores Lógicos

Os operadores lógicos são usados para realizar operações lógicas, geralmente em condições. Veja a tabela abaixo para entender melhor cada operador:

| Operador | Nome        | Descrição                                                        |
|----------|-------------|------------------------------------------------------------------|
| &&       | E lógico    | Retorna verdadeiro se ambos os operandos forem verdadeiros       |
| \|\|     | OU lógico   | Retorna verdadeiro se pelo menos um dos operandos for verdadeiro |
| !        | NÃO lógico  | Inverte o valor lógico do operando                               |

Exemplos:

```go
a := true
b := false
fmt.Println(a && b) // Saída: false
```

```go
a := true
b := false
fmt.Println(a || b) // Saída: true
```

```go
a := true
fmt.Println(!a) // Saída: false
```

## Finalização

Nesta aula, exploramos os principais operadores em GoLang, incluindo operadores aritméticos, de atribuição, lógicos e de comparação. Compreender esses operadores é essencial para criar condições e manipular variáveis em seus programas. Continue praticando e aplicando esses conceitos em seus projetos para se tornar profissional em GoLang. 

Até a próxima aula e boa codificação! 🚀


