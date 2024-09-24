---
author: Gabriel Moodlight
pubDatetime: 2024-08-17T22:00:00.000Z
modDatetime: 2024-08-17T22:00:00.000Z
title: "Git Stash - Salve suas mudanças como um profissional!"
slug: git-stash
featured: false
draft: false
tags:
 - git
 - dicas
description: Domine o poder do git stash para gerenciar suas mudanças de código com eficiência!
---

# Salvando suas Mudanças como um Pro 🚀

O comando `git stash` é uma ferramenta incrível que permite salvar mudanças temporariamente em seu repositório sem fazer um commit. Ele é especialmente útil quando você precisa alternar entre branches rapidamente ou começar a trabalhar em outra tarefa sem perder suas alterações não finalizadas.

> 💡 **Dica:** Se você não está familiarizado com Git, recomendo que leia [este artigo da Alura](https://www.alura.com.br/artigos/o-que-e-git-github) antes de continuar.


## O Básico do `git stash`

Vamos começar com o básico. Quando você executa o comando `git stash`, ele realiza as seguintes ações:

1. Captura as mudanças no seu diretório de trabalho e na área de staging
2. Salva essas mudanças em um stash
3. Reverte seu diretório de trabalho para o estado do último commit

```bash
git stash
```
Após executar este comando, seu diretório de trabalho estará limpo, mas suas alterações não foram perdidas - elas foram armazenadas em uma "pilha" de stashes.

## Recuperando suas Mudanças
Para recuperar suas mudanças, você pode usar o comando `git stash apply`, que aplica o stash mais recente ao seu diretório de trabalho.

```bash
git stash apply
```
Se você quiser aplicar um stash específico, use `git stash list` para ver todos os stashes disponíveis e recupere o que deseja.
```bash
git stash list
git stash apply stash@{n}  # onde 'n' é o número do stash
```

## Práticas Avançadas

### Criando um stash com uma mensagem
Para melhor organização, você pode adicionar uma mensagem descritiva ao seu stash:
```bash
git stash save "Descrição das mudanças stashadas"
```

### Removendo um Stash
Após aplicar um stash, você pode querer removê-lo da pilha:
```bash
git stash drop stash@{n}
```

### Aplicar e Remover em um Único Comando
O comando git stash pop aplica o stash mais recente e o remove da pilha:
```bash
git stash pop
```

## Conclusão

Dominar o `git stash` pode melhorar significativamente seu fluxo de trabalho, permitindo que você alterne entre tarefas com facilidade e mantenha seu repositório organizado. Pratique esses comandos e integre-os à sua rotina de desenvolvimento para maximizar sua produtividade.

---

### Links Úteis

<a href="https://git-scm.com/docs/git-stash" target="_blank">Documentação oficial do Git Stash</a>

<a href="https://atlassian.com/git/tutorials/saving-changes/git-stash#stashing-your-work" target="_blank">[Atlassian] Git Stash Tutorial Interativo</a>

---