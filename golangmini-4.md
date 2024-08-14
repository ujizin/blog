---
author: Jean Branco
pubDatetime: 2024-08-10T21:00:30.000Z
modDatetime: 2024-08-10T21:00:30.000Z
title: Tipos de Dados Básicos do Golang
slug: golangmini-tiposdedados
featured: false
draft: false
tags:
 - golang
 - backend
 - minicurso
description: Aprenda os tipos básicos essenciais da linguagem Go.
--- 

# GoLang MiniCurso - Aula 4: Tipos de Dados

Olá! Seja bem-vindo(a) a mais uma aula do MiniCurso de Go! Nesta aula, vamos ver de forma aprofundada sobre os Tipos de Dados na linguagem Go e outros conceitos importantes. Bora começar!?

## O que são Tipos de Dados?

O tipo de dado define o valor que será passado para uma variável. Em GoLang, existem 3 tipos básicos fundamentais que você precisa saber:

- **String:** Armazena cadeias de caracteres, geralmente textos.
- **Numéricos (int/float):** Representa números inteiros positivos e negativos, e números reais também positivos e negativos.
- **Boolean:** Representa um valor lógico, ou é verdadeiro (true) ou é falso (false).

> Existem muitos outros tipos, alguns até um pouco avançados, que você pode explorar pesquisando.

### Strings

Uma String armazena sequências de caracteres, que geralmente são textos. Esses caracteres sempre estão delimitados por aspas duplas (`""`), contendo o conteúdo ou os caracteres por dentro. Veja os exemplos a seguir e compreenda melhor:

```go
var minhaString1 string = "Olá, mundo!" // Definimos um tipo para a variável que será do tipo string com a palavra-chave "string"
var minhaString2 string = "GoLang é uma linguagem fenomenal!"
var minhaString3 string = "23" // Qualquer caractere armazenado em String "" (incluindo números) sempre será string!

fmt.Println(minhaString1)
fmt.Println(minhaString2)
fmt.Println(minhaString3)
```

```go
fmt.Println("GoLang possui Tipagem Estática Forte")
fmt.Println("MiniCurso de GoLang :)")
```

```go
fmt.Println("3ss4 str1ng p0ss81 n8m3r0s n0 l8ug4r d4s v0g41s.")
```

> Conseguiu entender bem como uma String funciona? Se você não entendeu, pratique em sua máquina, isso vai te ajudar depois.

### Integers (Inteiros)

Integers ou int, é um tipo de dado numérico que armazena valores inteiros, que podem ser positivos e negativos. Veja os exemplos:

```go
var meuInt1 int = 1204222 // Definimos um tipo para a variável que será do tipo inteiro com a palavra-chave "int"
var meuInt2 int = 2233
var meuInt3 int = 194858358
var meuInt4 int = 0
var meuInt5 int = -2485 
var meuInt6 int = -39955995
```

> O `int` possibilita você digitar números de qualquer comprimento, sendo positivos ou negativos.

### Float (Flutuante)

Float ou flutuante, é um tipo de dado numérico que armazena valores reais, com ponto flutuante, que também podem ser positivos e negativos. Veja os exemplos e entenda melhor:

```go
var meuFloat1 float64 = 10.5 // Definimos um tipo para a variável que será do tipo flutuante com a palavra-chave "float64"
var meuFloat2 float64 = 0.42858 
var meuFloat3 float64 = 1034696496.86
var meuFloat4 float64 = -1394.4858
var meuFloat5 float64 = -19.4548584868846
```

> O `float` permite você digitar números de qualquer comprimento, assim como o `int`.

### Boolean (Booleano)

Boolean ou bool, é um tipo de dado que representa valores lógicos. Toda a variável do tipo boolean possui o valor "true" (verdadeiro) ou "false" (falso). Veja um exemplo para entender melhor.

```go
var meuBool1 bool = true
var meuBool2 bool = false
var meuBool3 bool = true
```

> Se você nunca programou, deve estar se perguntando: "Pra que isso existe?". Na verdade, o "bool" será seu parceiro na programação até o fim dos tempos e sempre estará em seus códigos, pois a todo momento lidamos com valores lógicos. Mais pra frente, você verá o "bool" melhor e mudará sua opinião.

## Finalização

Chegamos ao final de mais uma aula! Espero que você tenha entendido e praticado com os tipos ensinados para fixá-los na sua mente, pois esta aula apenas introduziu os tipos de dados básicos. Ainda existem muitos pela frente que você pode pesquisar.

Até a próxima aula e boa codificação! 🚀
