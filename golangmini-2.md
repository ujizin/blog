---
author: Jean Branco
pubDatetime: 2024-08-10T21:00:00.000Z
modDatetime: 2024-08-10T21:00:00.000Z
title: Compreendendo Variáveis em GoLang
slug: golangmini-variaveis
featured: false
draft: false
tags:
 - golang
 - backend
 - instalacao
 - minicurso
description: Entenda como usar variáveis na linguagem GoLang e suas principais características.
--- 

# GoLang MiniCurso - Aula 2: Variáveis

Olá! Seja bem-vindo a mais uma aula do MiniCurso de Golang! Nesta aula, vamos explorar de forma detalhada o que são variáveis e alguns conceitos relacionados. Vamos começar?

## O que são Variáveis?

Variáveis são espaços na memória do seu computador que armazenam valores para uso posterior. Em termos simples, uma variável é como uma prateleira onde você pode guardar um item. Cada item na prateleira tem um `Identificador`, um `Valor` e um `Tipo`. Imagine uma prateleira com um carrinho de brinquedo: o identificador é `carrinho`, o valor é `Carrinho da Hotwheels`, e o tipo é `Brinquedo`.

## Tipos de Variáveis

Antes de usar variáveis, é importante entender os principais tipos de variáveis em Golang:

- **string:** Cadeia de caracteres, geralmente usada para textos. Exemplos: `"Olá"`, `"Eu sou Pedro"`, `"Golang é uma linguagem moderna"`.
- **int:** Números inteiros, tanto positivos quanto negativos. Exemplos: `24`, `-274`, `0`, `123456`.
- **bool:** Valores lógicos, que podem ser `true` ou `false`.
- **float64:** Números com ponto flutuante (decimais), positivos e negativos. Exemplos: `23.9`, `59.3885`, `-8485.249`.

## Declarando Variáveis

Declarar uma variável reserva um espaço na memória para ela ser usada mais tarde.

```go
var nome string // Declarando uma variável com o identificador "nome" do tipo "string"
var idade int   // Declarando uma variável com o identificador "idade" do tipo "int"
```

> Com isso, reservamos dois espaços na memória para as variáveis e agora podemos atribuir valores a elas.

## Atribuição de Valor

Após declarar uma variável, podemos atribuir um valor a ela. Sem valor, a variável não será útil em nosso programa.

```go
var nome string // Declarando a variável
var idade int   // Declarando a variável

nome = "João"   // Atribuindo valor à variável (no caso, uma string)
idade = 20      // Atribuindo valor à variável (no caso, um int)
```

> Lembre-se de que, em Golang, variáveis declaradas devem ser utilizadas. Caso contrário, o compilador apontará um erro.


## Declarando e Atribuindo Valor

É possível declarar e atribuir um valor a uma variável em uma única linha de código usando o operador de atribuição `=`.

```go
var nome string = "João" // Declarando e atribuindo valor
var idade int = 20
```

> Na maioria dos casos, usaremos a declaração e atribuição em uma única linha. Apenas em casos específicos a variável não terá um valor inicial.

## Reatribuindo Valor

Após a variável ser declarada, você pode modificá-la conforme necessário em seu programa. Veja um exemplo:

```go
var nome string = "Pedro" // Declarando com um valor inicial

nome = "Maria" // Reatribuindo valor 
nome = "Isabela"
```

```go
nome := "Matheus" // Declaração e atribuição com forma curta

nome = "Gabriel"
nome = "Lucas"
nome = "Murilo"
```

> Após a declaração inicial, não é possível redeclarar a variável com o operador := ou a palavra-chave var. Somente a atribuição de novo valor é permitida, pois a declaração reserva o espaço na memória.

## Imprimindo o Valor da Variável

Se o seu editor de código, como o VS Code, apontar erro para a variável, é porque ela foi declarada mas não utilizada. Para evitar isso, você pode imprimir o valor da variável usando a função `Println` do pacote `fmt`.

```go
package main

import "fmt"

func main() {
    var nome string
    nome = "Bruno"
    fmt.Println(nome) // Imprime o valor contido na variável "nome", que é "Bruno"
}
```

## Formas de Declarar Variáveis

Em Go, existem duas formas principais de declarar variáveis:

**Forma curta (com operador `:=`):**

```go
nome := "Jean" // Declarando a variável "nome" e atribuindo o valor "Jean"
fmt.Println(nome) // Imprimindo a variável no console
```

> A forma curta é chamada de **declaração com tipo implícito**, pois o tipo da variável é inferido a partir do valor atribuído, ou seja, o compilador Go decide o tipo da variável para você.

**Forma extensa (utilizando a palavra-chave `var`):**

```go
var nome string = "Jean" // Declarando a variável "nome" do tipo "string" e atribuindo o valor "Jean"
fmt.Println(nome) // Imprimindo a variável no console
```

> A forma extensa é chamada de declaração com tipo explícito, pois o tipo da variável é especificado pelo desenvolvedor. Uma vez que a variável é definida com um tipo, não será possível atribuir um valor de tipo diferente a ela.

## Implícito X Explícito

Em Golang, a escolha do tipo de declaração deve ser feita com base no contexto:

**Implícito:**
- Usado apenas dentro de **funções**.
- Não pode ser declarado sem atribuir valor.

```go
func main() {
    nome := "Matheus" // Usado apenas dentro da função, e deve ter um valor inicial.
}
```

**Explícito:**
- Pode ser usado dentro e fora de **funções**.
- Pode ser declarado sem atribuir valor inicial.

```go
var nome string = "Igor"

func main() {
    var idade = 30
    fmt.Println(nome, idade)
}

```

> Cada tipo de declaração tem seus casos específicos de uso. A declaração explícita é mais legível, pois o tipo é claramente especificado, enquanto a declaração implícita deixa o tipo para o compilador decidir.

## Tipagem Estática Forte

Golang é uma linguagem de tipagem estática forte. Isso significa que, uma vez que uma variável é declarada com um tipo, você não pode atribuir um valor de tipo diferente a ela.

```go
var variavel string // Definindo explicitamente que "variavel" será do tipo "string"

variavel = "Olá" // Atribuindo valores do tipo "string"
fmt.Println(variavel)

variavel = "Casa"
fmt.Println(variavel)

variavel = "Mundo"
fmt.Println(variavel)

variavel = 20 // O programa irá parar aqui por causa de um erro de tipo
fmt.Println(variavel)

variavel = "285" // Este ponto nunca será alcançado devido ao erro anterior
fmt.Println(variavel)
```

```go
variavel := 12 // Declaração implícita com valor "12", o compilador define que a variável é do tipo "int"
fmt.Println(variavel)

variavel = -475
fmt.Println(variavel)

variavel = -1747
fmt.Println(variavel)

variavel = "Olá" // O programa irá parar aqui devido a um erro de tipo
fmt.Println(variavel)
```

> Linguagens como JavaScript ou Python possuem tipagem dinâmica, permitindo que uma variável altere seu tipo após a declaração. Contudo, a tipagem estática de Go ajuda a evitar erros de tipo e promove a segurança do tipo em tempo de compilação.

## Regras de Nomenclatura

Ao nomear variáveis, é importante seguir algumas boas práticas e regras da linguagem:

**Boas Práticas:**
- Use nomes descritivos (ex: idade, precoProduto, carName).
- Evite nomes genéricos ou pouco informativos (ex: num1, pessoa1).
- Evite nomes muito curtos ou abreviados (ex: num, nom, x, y).

**Regras de Nomenclatura:**
- Um nome de variável deve começar com uma letra ou com um caractere sublinhado (_).
- Nomes de variáveis não podem começar com números.
- Nomes de variáveis podem conter apenas caracteres alfanuméricos e sublinhados (a-z, A-Z, 0-9, e _).
- Nomes de variáveis diferenciam maiúsculas de minúsculas (idade, Idade, IDADE são três variáveis diferentes).
- Nomes de variáveis não podem conter espaços.
- Nomes de variáveis não podem ser palavras reservadas (ex: package, func, import).

### Formas de Nomear Variáveis:

**Camel Case:** Cada palavra, exceto a primeira, começa com letra maiúscula:

```go
meuNomeCompleto := "Jean Lourenço Branco"
```

**Pascal Case:** Cada palavra começa com letra maiúscula:

```go
MeuNomeCompleto := "Jean Lourenço Branco"
```

**Snake Case:** Cada palavra é separada por um caractere sublinhado (_):

```go
meu_nome_completo := "Jean Lourenço Branco"
```

> Cada forma de nomenclatura pode ser usada dependendo do contexto e das convenções adotadas pela equipe ou projeto.

## Finalização

Parabéns! Você chegou ao final da aula. Embora possa parecer um pouco cansativo, agora você tem um entendimento sólido sobre variáveis em Golang. Lembre-se de praticar para fixar os conceitos e aplicá-los em seus projetos futuros.

Até a próxima aula e boa codificação! 🚀
