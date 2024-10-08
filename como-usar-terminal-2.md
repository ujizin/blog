---
author: Humberto (op3n)
pubDatetime: 2024-09-28T13:46:35.000Z
modDatetime: 2024-09-28T13:46:35.000Z
title: "Como usar o terminal Linux? (Parte 2)"
slug: como-usar-terminal-linux-2
featured: false
draft: false
tags:
 - backend
 - iniciantes
 - linux
 - basico
 - minicurso
description: Como usar o seu aliado secreto do linux? Aqui você vai entender como usar o terminal!
---



# Tópico 1 ("O começo do fim!")

Hey meu amigo dev, seja bem vindo novamente ao *Cap 02* de como usar o terminal!
Bem, no último artigo, você aprendeu os comandos, e como usar o gestor de arquivos do Linux (Ubuntu Based), e inclusive, por falar em Ubuntu Based, você também aprendeu o que são distros, o que são distros baseados em linux, e o que são distros baseados em outras distros. Para finalizar, eu dei a sugestão de você aprender sobre o Git!

Agora, você está no segundo artigo, aqui, vou falar um pouco sobre a parte mais densa do linux, alguns arquivos importantes, sintaxe, e dentre muitas outras coisas, então sem mais enrolação, simbora aprender!

---


# Tópico 2 ("A teoria prática")

Essa é a hora que você abre o terminal, porque lá vem algumas coisas teóricas mas que enquanto você entende a teoria, você vai usa-los na prática!

---

### 1° Comando "echo"
O comando echo, pode te ajudar a escrever coisas na tela (Similar ao print("") do python), escrever textos nos arquivos, e dentre muitas coisas!

**Sintaxe "echo"**
A sintaxe é `echo "Olá Mundo!"` para mostrar algo na tela, o que, na prática, deve ser assim:
```
humberto@pop-os:~$ echo "Olá Mundo!"
Olá Mundo!
```

Agora que você entendeu como ele funciona, vamos usa-lo para gravar dados em arquivos:
A sintaxe seria `echo "Lorem Ipsum etc e tals" > arquivo.txt`

---


Compreendendo o comando:
```
echo - Comando que você está aprendendo
"Texto" - O que deve ser gravado no arquivo
> - Dentro do arquivo
arquivo.txt - nome do arquivo
```
O comportamento experado seria:

```
humberto@pop-os:~$ echo "Lorem Ipsum etc e tals" > arquivo.txt
humberto@pop-os:~$ 
```

Por último, o **echo** pode ler variáveis de ambiente
Usando: 
```
echo $PATH
```
Esse comando lê a variável de ambiente PATH, que em resumo, é aonde fica todas as pastas que contém comandos do seu terminal.

E como eu leio esse arquivo? Aí é que chegamos no nosso segundo comando.

---

### 2° Comando: "cat"

O comando **cat** tem o objetivo de ler alguns arquivos, porém não lê variaveis de ambiente, então eu quero te desafiar, vou te ensinar a usar esse comando, e depois fazer uma pergunta objetiva com 4 alternativas de quais comandos podem criar arquivos (**echo**) e depois ler o que tem dentro desse arquivo usando o (**cat**).
O comando **cat** tem uma sintaxe relativamente simples.

---

**A sintaxe**

Para ler o arquivo `teste.txt` por exemplo, podemos usar:
```
humberto@pop-os:~$ echo "Esse arquivo de teste, está com esse conteúdo." > teste.txt
humberto@pop-os:~$ cat teste.txt
Esse arquivo de teste, está com esse conteúdo.
humberto@pop-os:~$ 
```


Sabendo disso, vamos para "**o desafio**"

---

#### O desafio!

Como podemos criar um arquivo, colocar algo dentro dele, e depois ler ele?
```
A: echo "Lorem Ipsum" < teste.txt / cat teste.txt
B: echo "Lorem Ipsum" > teste.txt / cat < teste.txt
C: echo "Lorem Ipsum" > teste.txt / cat teste.txt
D: echo Lorem Ipsum == teste.txt / cat teste.txt
```

Se você achou que a resposta correta era a D, errou! A resposta correta é a C. Porque as outras estão incorretas?

```
A: echo "Lorem Ipsum" < teste.txt / cat teste.txt

O caractere "<", nesse comando, não segue este propósito, nesse caso o correto seria ">"

B: echo "Lorem Ipsum" > teste.txt / cat < teste.txt

O comando cat, não pode utilizar o caractere "<", assim apenas funcionando caso elimine o caractere.

D: echo Lorem Ipsum == teste.txt / cat teste.txt

No bash, não utilizamos o "==", o igual, além de não se aplicar a esse propósito, quando precisamos usar, é apenas 1 "="

```

---

### 3° Comando "export"

O comando **`export`**, serve para diversos propósitos, e dentre eles, definir variáveis!
Então vamos entender a sintaxe.

```
export nome="Humberto"
```

Esse comando define a variavel nome como Humberto, e assim, pode ser lido com o comando:

```
echo $nome
```

E para deletar uma variavel, usamos:

```
export nome=""
```

---

### 4° "Operadores"

No bash, você provavelmente vai querer rodar mais de um comando de uma vez, e aí que vem os operadores!
Os operadores existentes são:
**||** - Esse operador, executa dois comandos ao mesmo tempo, ou até mais, mas caso um comando falhe ou dê erro, a sequencia de comandos não é interrompida!
**&&** - Esse operador, igual ao **||**, executa dois ou mais comandos ao mesmo tempo, porém, caso um comando da sequencia dê erro, ele é interrompido!

---


#### Operadores na prática!

Digamos, que estamos prestando uma ajuda a nosso amigo, que quer instalar o cmatrix, e em seguida roda-lo, porém, caso dê erro, queremos que o script seja interrompido.
```
sudo apt install cmatrix && cmatrix
```

Porém, aogra vamos imaginar o mesmo cenário, porém caso dê erro, ele deve continuar a sequência.
```
sudo apt instal cmatrix || cmatrix
```


# Finalização

Parabéns! Eu fico admirado com a sua vontade de aprender! Graças a sua vontade de aprender, você leu 2 artigos, e agora, você sabe como usar o `apt`, como criar pastas, deletar pastas, a história do linux, o que é distro, como editar arquivos usando o `nano`, sabe como usar o `cat`, sabe como usa o `echo`, e ainda aprendeu sobre operadores! Agora, você está pronto para colocar a mão da massa, e você já consegue seguir sua jornada de estudos sozinho ou sozinha! Agradeço por ter lido!

# [Teste seus conhecimentos nessa provinha que fiz para vocês!](https://wordwall.net/pt/resource/78857017)
