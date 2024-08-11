---
author: Jean Branco
pubDatetime: 2024-08-10T21:00:20.000Z
modDatetime: 2024-08-10T21:00:20.000Z
title: Entrada e Saída de Dados em GoLang
slug: golangmini-entradasaida-dados
featured: false
draft: false
tags:
 - golang
 - backend
 - minicurso
description: Descubra como gerenciar entrada e saída de dados na linguagem GoLang.
--- 

# GoLang MiniCurso - Aula 3: Entrada de Dados & Saída de Dados

Olá!! Seja muito bem-vindo(a) à mais aula do MiniCurso de Go! Nesta aula, vamos nos aprofundar em **Entrada e Saída de Dados**, entendendo como funciona e como utilizá-las na prática. Vamos começar!?

## Saída de Dados

A saída de dados, ou **Output**, refere-se a todos os dados que são impressos no console do nosso programa. Toda vez que utilizamos funções como `Print`, `Println`, e `Printf`, estamos gerando saída de dados.

### Print

A função `Print` está inclusa no pacote `fmt` e imprime na tela os argumentos/valores com a formatação padrão. Veja os exemplos a seguir para entender melhor:

```go
var a, b string = "Hello", "World"

fmt.Print(a)
fmt.Print(b)

// Saída: 
// HelloWorld
```

> O `Print` não pula nenhuma linha no final e não separa argumentos por espaços. Isso deve ser feito manualmente!

```go
var a, b string = "Hello", "World"

fmt.Print(a, " ", b) // Separamos os dois argumentos com um espaço em branco.

// Saída:
// Hello World
```

```go
var a, b string = "Hello", "World"

fmt.Print(a, "\n", b) // Utilizamos \n para quebrar a linha.

// Saída:
// Hello
// World
```

```go
fmt.Print("Essa mensagem\n será escrita em multiplas\n linhas usando a instrução\n mencionada.\n")

// Saída:
// Essa mensagem
// será escrita em multiplas
// linhas usando a instrução
// mencionada.
```

> "\n" é uma instrução usada em strings para criar novas linhas, independentemente da quantidade usada em uma string.

```go
var x, y int = 2, 5

fmt.Print(x, y)

// Saída:
// 25
```

> O Go apenas insere espaços se nenhum dos argumentos for string.

### Println

A função `Println` é semelhante ao `Print`, com a diferença de que adiciona um espaço em branco entre os argumentos e uma nova linha no final. Veja os exemplos:

```go
var x, y, z string = "Hello", "World", "Golang"

fmt.Println(x, y)
fmt.Println(z)

// Saída:
// Hello World
// Golang
```

> O Println automaticamente pula uma linha no final da saída. Além disso, você pode usar a instrução \n para formatar a saída conforme necessário.

## Entrada de Dados

A entrada de dados, ou **Input**, refere-se aos dados digitados pelo usuário que podem ser capturados e armazenados em variáveis para processamento posterior.

### Scan

A função `Scan`, que também está no pacote `fmt`, permite a leitura de dados digitados pelo usuário e o armazenamento desses dados em variáveis. Veja os exemplos a seguir:

```go
var nome string 

fmt.Println("Digite seu nome:")
fmt.Scan(&nome) 

fmt.Println("Seu nome é", nome)
```

```go

var carroModelo, carroMarca string

fmt.Println("Qual é o modelo do carro?")
fmt.Scan(&carroModelo)
fmt.Println("Qual é a marca do carro?")
fmt.Scan(&carroMarca)

fmt.Printf("O modelo do carro é", carroModelo, "e a marca é", carroMarca)
```

> O `&` antes do nome da variável é crucial, pois indica o endereço da variável na memória para que Scan possa armazenar o valor nela.

Existem outras funções de `Scan` que oferecem diferentes comportamentos, mas não vamos abordá-las nesta aula. Você pode explorar mais sobre elas se desejar.

## Finalização

Chegamos ao final de mais uma aula. Hoje você aprendeu sobre Entrada e Saída de Dados e está pronto para os desafios propostos. Preparei **3 desafios** para você, que estarão nesse repositório na pasta `desafios`. Recomendo fortemente que você complete esses desafios e baixe o material adicional para consolidar seu aprendizado em GoLang.

Espero que tenha gostado da aula! Até a próxima.
