---
author: Gabriel Moodlight
pubDatetime: 2024-08-02T02:00:00.000Z
modDatetime: 2024-08-02T05:00:00.000Z
title: NPM - Entenda!
slug: npm-entenda
featured: false
draft: false
tags:
 - npm
 - node
 - javascript
description: Aprenda os conceitos básicos de uma vez por todas!
---

E aí, galera do código! 🚀

Se você é usuário de JavaScript (e entenda usuário como quem usa, seu viciado), certamente já se deparou com o NPM, certo? Neste artigo, vamos explorar como essa ferramenta fantástica pode facilitar o seu trabalho e tornar sua vida como desenvolvedor muito mais prática.

## O que é?
NPM, que em 2010 foi criada por Isaac Z. Schlueter, significa Node Package Manager. É basicamente um gerenciador de pacotes para o Node. Com ele, é possível instalar, atualizar e gerenciar bibliotecas e módulos de forma simples e eficiente. Se já usou pip no Python ou Composer no PHP, o conceito será fácil de entender.

## Por que usar?
Imagine que está construindo um aplicativo e precisa de funcionalidades específicas, como fazer requisições HTTP ou manipular datas. Em vez de escrever tudo do zero, pode-se usar pacotes prontos que outras pessoas já escreveram. Isso economiza tempo e esforço, além de possibilitar foco nas partes mais específicas do projeto.

## Instalação
Primeiramente, para usar o NPM, é necessário ter o Node instalado. Normalmente, o NPM já vem junto com o Node.js. Verifique se o NPM está instalado na sua máquina rodando o seguinte comando no terminal:

```bash
npm -v
```
Isso deve mostrar a versão do NPM instalada. Se ainda não tem o Node.js/NPM instalado, pode baixá-los em <a href="https://nodejs.org/" target="_blank">nodejs.org</a>

# Comandos Básicos
Vamos aprender alguns comandos básicos para começar a usar o NPM no dia a dia.

## `npm init`
Esse comando inicia um novo projeto Node e cria um arquivo `package.json`.

Para iniciar um projeto, use o seguinte comando:
```bash
npm init
```
Siga as instruções no terminal, passando as informações do seu projeto.
> Se quiser pular as perguntas e gerar um arquivo `package.json` padrão, use `npm init -y`.

## `npm install`
Esse comando instala pacotes Node na sua aplicação. Esses pacotes também são chamados de dependências.
```bash
npm install express
```
Isso adiciona o Express ao projeto e atualiza o `package.json` com essa dependência. Além disso, cria (ou atualiza) uma pasta `node_modules` onde o pacote será armazenado.

#### Dependências de Desenvolvimento
Alguns pacotes podemos usar apenas durante o desenvolvimento, como ferramentas de teste ou linters.

Para instalar essas dependências, use a flag `--save-dev` ou `-D`:
```bash
npm install jest --save-dev
# ou
npm install jest -D
```

## `npm uninstall`
Esse comando desinstala um pacote/dependência da sua aplicação e a remove do `package.json`;
```bash
npm uninstall express
```

## `npm update`
Esse comando atualiza todas as dependências do projeto para as últimas versões disponíveis,
respeitando as restrições definidas no `package.json`.
```bash
npm update
```

## `npm run`
O npm run é usado para executar scripts definidos no `package.json`. Por exemplo, é possível ter um script para iniciar o servidor e outro para testar:
```json
"scripts": {
  "start": "node index.js",
  "test": "jest test.js"
}
```
E então, no terminal, execute:
```bash
npm start
# ou
npm run test
```

## Explorando o NPM Registry
O NPM possui um registro online onde é possível encontrar milhares de pacotes. Para buscar pacotes, use o site <a href="https://www.npmjs.com/" target="_blank">npmjs.com</a> ou o comando de busca:
```bash
npm search nome-do-pacote
```
Por exemplo, para buscar pacotes relacionados a validação de dados, execute:
```bash
npm search validation
```

## 📦 Arquivos e Pacotes
### `package.json`
O `package.json` é o coração do seu projeto Node. Ele mantém um registro das dependências, scripts e informações do projeto, como nome e versão. É onde você define o que seu projeto precisa para funcionar e como ele deve ser executado.
### `package-lock.json`
O `package-lock.json` é o guardião das versões **exatas** das suas dependências. Ele garante que todos que trabalham no projeto tenham as mesmas versões das bibliotecas, evitando surpresas e problemas de compatibilidade.
### `node_modules`
A pasta `node_modules` é onde todas as suas dependências são instaladas. Quando você executa `npm install`, as bibliotecas listadas no `package.json` são baixadas e colocadas aqui. O arquivo `package-lock.json` também é gerado neste momento.

Essa pasta pode crescer bastante, então evite incluí-la no controle de versão.
> Em alguns projetos, pode-se optar por não versionar o `package-lock.json` para permitir atualizações mais flexíveis das dependências. No entanto, isso pode levar a inconsistências de versão. *Avalie a melhor abordagem para o seu fluxo de trabalho.*

## Dicas e Truques
 - Use versões específicas: Para evitar problemas de compatibilidade, defina versões específicas dos pacotes no `package.json`.
 - Scripts úteis: Crie scripts personalizados no `package.json` para tarefas comuns, como iniciar o servidor, rodar testes, etc.
 - Leia a documentação: Sempre dê uma olhada na documentação dos pacotes que está usando para entender todas as funcionalidades e configurações.

## Conclusão
O NPM é uma ferramenta poderosa que facilita muito o gerenciamento de dependências no desenvolvimento com Node. Com os comandos básicos que foram apresentados, é possível iniciar e gerenciar projetos de forma eficiente. Espero que essa aula tenha sido útil e que agora você se sinta mais confortável para usar o NPM no dia a dia.

<!-- Qualquer dúvida, deixe nos comentários! -->

Até a próxima!

---

### Links Úteis:

<a href="/posts/bun-novo">Bun - O novo queridinho dos devs JS!</a>

<a href="https://docs.npmjs.com/" target="_blank">Documentação oficial do NPM</a>

<a href="https://nodejs.org/" target="_blank">Site oficial do Node.js</a>

<a href="https://www.npmjs.com/" target="_blank">NPM Registry</a>

<a href="https://www.treinaweb.com.br/blog/10-truques-do-npm-voce-conhece-todos" target="_blank">[TreinaWeb] 10 Truques do NPM</a>

<a href="https://www.alura.com.br/artigos/criando-e-publicando-uma-biblioteca-javascript-no-npm" target="_blank">[Alura] Criando e Publicando uma Lib no NPM</a>

---
