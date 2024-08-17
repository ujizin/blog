---
author: Jean Branco
pubDatetime: 2024-08-10T21:00:00.000Z
modDatetime: 2024-08-10T21:00:00.000Z
title: Introdução ao GoLang
slug: golangmini-introducao
featured: false
draft: false
tags:
 - golang
 - backend
 - instalacao
 - minicurso
description: Aprenda a instalar e começar a usar o GoLang.
--- 

# GoLang MiniCurso - Aula 1: Introdução ao Golang

Olá! Seja bem-vindo(a) à primeira aula do MiniCurso de Golang. Nesta aula, você vai descobrir o que é o Golang, aprender como configurá-lo na sua máquina, escreverá seu primeiro programa e entenderá como funciona um programa Go. Vamos começar?

## O que é o Golang?

**Golang**, ou simplesmente **Go**, é uma linguagem de programação de código aberto desenvolvida pelo Google em 2007. Go é conhecida pela sua simplicidade e eficiência, tornando-a uma escolha popular para o desenvolvimento de servidores web e aplicações em nuvem.

### Características principais do Golang:

- **Simplicidade:** Possui uma sintaxe clara e fácil de aprender.
- **Desempenho:** Oferece uma compilação rápida e execução eficiente.
- **Biblioteca Padrão:** Vem com uma biblioteca padrão rica em funcionalidades.

## Iniciando com Golang

### Passo 1: Instalar e Configurar o Golang

1. Acesse o [site oficial do Golang](https://go.dev/) e baixe a versão mais recente da linguagem para o seu sistema operacional.
2. Confira a [documentação de instalação](https://go.dev/doc/install) para orientações detalhadas conforme o sistema que você está utilizando.

### Passo 2: Configurando o Ambiente

1. **IDE / Editor de Código**

   Vamos usar o **Visual Studio Code** (VS Code) por ser gratuito e bastante prático. Certifique-se de que você já tenha o VS Code instalado.

2. **Instalando a Extensão `Go`**

   No VS Code, instale a extensão `Go`:
   - **Título:** Go
   - **Descrição:** Rich Go language support for Visual Studio Code
   - **Autor:** Go Team at Google

   Para instalar, vá para a aba de extensões no VS Code e busque por "Go". Instale a extensão oferecida pela equipe do Google.

### Passo 3: Criando o Primeiro Programa

1. Crie um diretório de trabalho para o seu projeto, por exemplo, `hello-world`.
2. Dentro deste diretório, crie um arquivo chamado `main.go`.
3. Insira o seguinte código no arquivo `main.go`:

```go
package main

import "fmt"

func main() {
   fmt.Println("Olá, mundo!")
}
```

4. Para compilar e executar seu programa, abra o terminal no diretório do seu projeto e execute o comando:

```bash
go run main.go
```

5. Você deve ver a seguinte saída:

```txt
Olá, mundo!
```

## Sintáxe

Um arquivo Go, possui:

- **Declaração de Pacotes:** Define o pacote ao qual o código pertence.
- **Importação de Pacotes:** Importa funcionalidades de pacotes externos.
- **Funções:** Blocos de código que executam ações específicas.
- **Declarações e Expressões:** Permitem criar variáveis e realizar operações.

Veja o código abaixo para entender melhor:

```go
package main 

import "fmt"

func main() {
   fmt.Println("Olá, mundo!")
}
```

**Código Explicado:**

- **Pacote:** Todo programa Go faz parte de um pacote. A palavra-chave `package` define o nome do pacote. Neste exemplo, o pacote é main.
- **Importação:** A palavra-chave `import` permite incluir pacotes que fornecem funcionalidades adicionais. Neste exemplo, importamos o pacote fmt para usar suas funções.
- **Função Principal:** `func main()` define a função principal, que é o ponto de entrada do programa. Todo o código dentro de {} será executado quando o programa for iniciado.
- **Função Println:** `fmt.Println()` é uma função do pacote fmt que imprime texto no console. No exemplo, ela exibe a mensagem **"Olá, mundo!"**.

## Finalização

Parabéns! 🎉 Você completou sua primeira aula do MiniCurso Golang. Agora você sabe o que é o Go, como configurar seu ambiente de desenvolvimento, criar um programa básico e entender a estrutura de um programa Go. Lembre-se de praticar para fixar os conceitos e aplicá-los em seus projetos futuros.

Até a próxima aula e boa codificação! 🚀
