---
author: Gabriel Moodlight
pubDatetime: 2024-07-17T05:00:00.000Z
modDatetime: 2024-07-17T05:00:00.000Z
title: Introdução ao TypeScript
slug: git-stash
featured: false
draft: true
tags:
 - git
 - dicas
description: Entenda o que é, como funciona e como usar TypeScript
---

## Dominando o `git stash` - Salvando suas Mudanças como um Pro 🚀

O comando `git stash` é uma ferramenta incrível que permite salvar mudanças temporariamente em seu repositório sem fazer um commit. Ele é especialmente útil quando você precisa alternar entre branches rapidamente ou começar a trabalhar em outra tarefa sem perder suas alterações não finalizadas.

### O Básico do `git stash`

Vamos começar com o básico. Quando você executa o comando `git stash`, ele pega as mudanças no seu diretório de trabalho e no índice (a área de staging) e as salva em um stash, limpando seu diretório de trabalho.

```bash
git stash
```
Após isso, seu diretório de trabalho estará limpo, mas as mudanças não foram perdidas; elas foram armazenadas em uma "pilha" de stashes.

### Recuperando suas Mudanças
Para recuperar suas mudanças, você pode usar o comando git stash apply, que aplica o stash mais recente ao seu diretório de trabalho.

```bash
git stash apply
```
Se você quiser aplicar um stash específico, use git stash list para ver todos os stashes disponíveis e recupere o que deseja.
```bash
git stash list
git stash apply stash@{n}  <!-- onde 'n' é o número do stash -->
```
