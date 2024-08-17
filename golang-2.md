---
author: Jean Branco
pubDatetime: 2024-08-03T20:00:10.000Z
modDatetime: 2024-08-03T20:00:10.000Z
title: Compreendendo Variáveis em GoLang
slug: golang-variaveis
featured: false
course: golang
draft: false
tags:
 - golang
 - backend
description: Entenda as variáveis em GoLang e suas principais características.
--- 

# GoLang - Aula 2: Variáveis

Olá! Seja bem-vindo a mais uma aula da nossa Trilha de Golang! Nesta aula, vamos explorar de forma detalhada o que são variáveis e alguns conceitos relacionados. Vamos começar?

## Tópicos da Aula:

- [O que são Variáveis](#o-que-são-variáveis)
- [Tipos de Variáveis](#tipos-de-variáveis)
- [Declarando Variáveis](#declarando-variáveis)
- [Atribuição de Valor](#atribuição-de-valor)
- [Declarando e Atribuindo Valor](#declarando-e-atribuindo-valor)
- [Reatribuindo Valor](#reatribuindo-valor)
- [Imprimindo o Valor da Variável](#imprimindo-o-valor-da-variável)
- [Formas de Declarar Variáveis](#formas-de-declarar-variáveis)
- [Implícito X Explícito](#implícito-x-explícito)
- [Tipagem Estática Forte](#tipagem-estática-forte)
- [Regras de Nomenclatura](#regras-de-nomenclatura)
- [Declaração de Multiplas Variáveis](#declaração-de-variáveis-múltiplas)
- [Declaração de Variáveis em Bloco](#declaração-de-variáveis-em-bloco)
- [Constantes](#constantes)

## O que são Variáveis?

Variáveis são espaços na memória do seu computador que armazenam valores para uso posterior. Em termos simples, uma variável é como uma prateleira onde você pode guardar um item. Cada item na prateleira tem um `Identificador`, um `Valor` e um `Tipo`. Imagine uma prateleira com um carrinho de brinquedo: o identificador é `carrinho`, o valor é `Carrinho da Hotwheels`, e o tipo é `Brinquedo`.

## Tipos de Variáveis

Antes de usar variáveis, é importante entender os principais tipos de variáveis em Golang:

- **string:** Cadeia de caracteres, geralmente usada para textos. Exemplos: `"Olá"`, `"Eu sou Pedro"`, `"Golang é uma linguagem moderna"`.
- **int:** Números inteiros, tanto positivos quanto negativos. Exemplos: `24`, `-274`, `0`, `123456`.
- **bool:** Valores lógicos, que podem ser `true` ou `false`.
- **float64:** Números com ponto flutuante (decimais), positivos e negativos. Exemplos: `23.9`, `59.3885`, `-8485.249`.

> Em futuras aulas, vamos explorar mais a fundo os tipos de dados, pois é um tópico extenso, assim como as variáveis.

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

## Declaração de Variáveis Múltiplas

Em Golang, você pode declarar várias variáveis na mesma linha. Isso é útil para melhorar a legibilidade.

```go
var a, b, c, d, e int = 2, 4, 6, 8, 10

fmt.Println(a)
fmt.Println(b)
fmt.Println(c)
fmt.Println(d)
fmt.Println(e)
```

> Quando declaramos várias variáveis do mesmo tipo, a declaração conjunta melhora a legibilidade. Também é possível declarar várias variáveis sem atribuir valores iniciais.

```go
var a, b, c int
var x, y, z string

a = 20
b = 11
c = 5
x = "C"
y = "C++"
z = "C#"

fmt.Println(a, b, c, x, y, z)
```

> Note que valores são atribuídos posteriormente. Isso é útil para declarar variáveis sem inicializar imediatamente.

## Declaração de Variáveis em Bloco

As declarações podem ser agrupadas em um bloco para evitar repetição da palavra-chave `var`.

```go
var (
    nome   string  = "João"
    idade  int     = 19
    altura float64 = 1.81
)
```

> Usar blocos para declarações pode economizar código e melhorar a organização.

Você também pode combinar declarações múltiplas e blocos.

```go
var (
    x, y, z int    = 2, 5, 11
    a, b, c string = "JS", "TS", "Node.js"
)

```

> Este método é útil para agrupar variáveis relacionadas e manter o código limpo e organizado.

## Constantes

Quando uma variável possui um valor fixo que não deve ser alterado, você pode usar a palavra-chave `const`. Uma constante é imutável após sua declaração.

```go
const minhaConstante string = "Golang" // A constante não pode ser alterada após a atribuição
fmt.Println(minhaConstante)
```
> Você não pode declarar uma constante sem atribuir um valor inicial. Além disso, a declaração de várias constantes em um bloco funciona da mesma forma que com variáveis.

## Finalização

Parabéns! Você chegou ao final da aula. Embora possa parecer um pouco cansativo, agora você tem um entendimento sólido sobre variáveis em Golang. Lembre-se de praticar para fixar os conceitos e aplicá-los em seus projetos futuros.

Até a próxima aula e boa codificação!
