---
author: Jean Branco
pubDatetime: 2024-07-17T05:00:00.000Z
modDatetime: 2024-07-17T05:00:00.000Z
title: Introdução ao TypeScript
slug: typescript-introducao
featured: false
draft: false
tags:
 - typescript
 - javascript
 - node
 - instalacao
description: Entenda o que é, como funciona e como usar TypeScript
---

# O que é o TypeScript?

TypeScript é um SuperSet (superconjunto) sintático do JavaScript, que possui a Tipagem Estática Forte, ou seja, permite com que os desenvolvedores adicionem tipos e tenham segurança durante o desenvolvimento do projeto.

- **SuperSet:** O TypeScript compartilha a mesma sintaxe do JavaScript, adicionando tipagem estática.
- **Compilação para JavaScript:** O TypeScript compila o código para .js (JavaScript), permitindo seu uso em qualquer ambiente onde o JavaScript é executado.

## Por que usar o TypeScript?

JavaScript é uma linguagem Fracamente Tipada, que acaba ficando difícil entender quais tipos estão sendo passados. Já o TypeScript, permite especificar os tipos de variáveis e argumentos de funções, aumentando a clareza e segurança do código.

### Vantagens do TypeScript

- **Especificação de tipos:** No TypeScript, você pode especificar o tipo de um argumento de função. Por exemplo, ao criar uma função que soma dois números, podemos especificar que a função só aceitará valores do tipo "number":

```ts
function sum(x: number, y: number): number { // Função com argumentos do tipo number, que retornará um valor do tipo number.
  return x + y;
}
```
- **Segurança durante o desenvolvimento:** O TypeScript alerta sobre erros de tipo antes da compilação, dependendo do editor de código em uso. Por exemplo, no Visual Studio Code, os erros são apontados antes mesmo de iniciar a compilação.
- **Verificação em tempo de compilação:** O TypeScript verifica se há algo errado durante a compilação, ajudando a evitar erros em tempo de execução.

# Como usar o TypeScript?

## Preparação do Ambiente

Entendeu o que é o nosso queridinho da web? Agora vamos aprender a preparar a nossa máquina para usar Typescript.

## 1º Passo - Instalando compilador TypeScript 

TypeScript é uma linguagem que compila para JavaScript usando um compilador chamado `TypeScript Compiler (TSC)`. Para instalar o compilador, é necessário ter o Node.js instalado em sua máquina e um arquivo `package.json` já criado no seu projeto. Se você não está familiarizado com o Node.js, é recomendado que comece por lá antes de prosseguir com o TypeScript para evitar complicações. Se o Node.js já está instalado, vamos continuar!

- Para instalar o TypeScript como dependência de desenvolvimento:
```txt
npm install typescript --save-dev
```

- Para instalá-lo como dependência global:
```txt
npm install typescript --global
```

> Recomendamos sempre instalar o TypeScript como dependência de desenvolvimento, pois é uma ferramenta que facilita o desenvolvimento do projeto.

## 2º Passo - Configurando o compilador TypeScript

Antes de começar a criar arquivos `.ts`, você precisará criar um arquivo de configuração para facilitar o desenvolvimento com TypeScript. As configurações do compilador são armazenadas em um arquivo chamado tsconfig.json. Por padrão, este arquivo não é criado automaticamente, então você deve criá-lo manualmente.

Você pode criar um arquivo `tsconfig.json` com as seguintes configurações básicas:
```json
{
  "include": ["src"],
  "compilerOptions": {
    "outDir": "./build"
  }
}
```

Para gerar um arquivo `tsconfig.json` com uma configuração padrão, digite o seguinte comando no terminal:
```txt
npx tsc --init
```

Como você está começando, pode ser mais fácil criar um arquivo `tsconfig.json` simples e adicionar as configurações conforme mencionado acima, para evitar confusão com configurações avançada

## 3º Passo - Compilando um arquivo TypeScript

Com o arquivo `tsconfig.json` configurado, crie uma pasta chamada `src` e adicione um arquivo com a extensão `.ts` dentro dessa pasta.

Você pode usar o seguinte script de exemplo para testar:
```ts
console.log("Olá, mundo!");
```

Para compilar o arquivo, digite o seguinte comando no terminal:
```txt
npx tsc
```

Após executar o comando, uma pasta chamada `build` será criada em seu projeto, contendo o arquivo `.js` compilado. Você pode executar este arquivo usando o `Node.js` ou integrá-lo ao seu projeto conforme necessário.

As configurações no `tsconfig.json` fazem o seguinte:
```json
{
  "include": ["src"], // Compila apenas os arquivos TypeScript existentes na pasta "src"
  "compilerOptions": {
    "outDir": "./build" // Compila os arquivos para a pasta "build"
  }
}
```

Essas configurações garantem que todos os arquivos na pasta src sejam compilados para a pasta build.

Se você não tiver um arquivo `tsconfig.json` e tentar rodar o comando `npx tsc`, você verá uma saída semelhante a esta:

```txt
Version 5.5.3
tsc: The TypeScript Compiler - Version 5.5.3
...
COMMON COMMANDS
...
```

A lista de comandos disponíveis será exibida, mas não haverá compilação de arquivos TypeScript.

Com o `tsconfig.json` presente, mesmo que esteja vazio, o compilador buscará e compilará arquivos .ts no diretório onde encontrou o arquivo .ts.

## Calmaí! Já está acabando
Até agora você viu:

- **TypeScript Compiler:** Como funciona o Compilador TypeScript
- **Instalação do Compilador:** Como instalar o Compilador TypeScript em seu projeto usando Node.js
- **Configuração do Compilador:** Como configurar o compilador para seu projeto, e algumas configurações úteis para facilitar o desenvolvimento.

# Agora é só praticar 🤓

Agora que já está tudo pronto, está na hora de você praticar!
Veja alguns exemplos de como utilizar Typescript para tipar os seus dados.

## Tipando Variáveis

O TypeScript permite especificar o tipo de uma variável para termos controle do valor passado e facilitar a legibilidade do código.

Veja o exemplo abaixo para compreender melhor:

```ts
const language: string = "JavaScript";    // Tipo String
const age: number = 29;                   // Tipo Number
const isFamous: boolean = true;           // Tipo Boolean

console.log(`O ${language} é uma linguagem de programação ${isFamous ? "famosa" : "desconhecida"} com ${age} anos de idade.`);
```

> Repare que para cada variável, adicionamos o `:` seguido do tipo que a variável vai ter. Se tentassemos passar um valor que não corresponde ao tipo, o arquivo não seria compilado e dispararia um erro.

## Tipando uma Função

O TypeScript requer que você tenha cuidado com as funções, pois precisamos especificar os tipos que os argumentos vão receber e também o tipo do retorno.

Veja abaixo:

```ts
// Parâmetros e retorno da função do tipo 'number'
function multiply(x: number, y: number): number {
  return x * y;
}

console.log(multiply(10, 4));
```

> Agora a função possui uma segurança enorme, pois não permite que seja passado como argumento valores além do tipo "number".