---
author: Gabriel Moodlight
pubDatetime: 2024-08-22T21:00:00.000Z
modDatetime: 2024-08-22T21:00:00.000Z
title: Progressive Web Apps (PWA)
slug: pwa
featured: false
draft: false
tags:
 - pwa
 - javascript
 - json
 - mobile
 - web
 - frontend
description: Você conhece as aplicações progressivas?
---


E aí, consultores de API! 🤓

Se você está pronto para levar suas habilidades de desenvolvimento web para o próximo nível, então os Progressive Web Apps (PWAs) são uma área que definitivamente merece sua atenção. Neste artigo, vamos mergulhar fundo no conceito de PWAs, explorar alguns exemplos práticos e ver como eles podem ser utilizados com frameworks modernos. Prepare-se para um conteúdo recheado de insights e práticas valiosas!

## O que é um PWA?
Um Progressive Web App é uma aplicação que combina o melhor das aplicações web e nativas para oferecer uma experiência rica e envolvente. PWAs são projetados para serem rápidos, confiáveis e adaptáveis, funcionando bem em qualquer dispositivo e em condições de rede variadas. Vamos ver os principais conceitos que definem um PWA:

### Características de um PWA
- **Progressivo**: Funciona em qualquer navegador, aproveitando o máximo das capacidades do navegador.
- **Responsivo**: Adapta-se a diferentes tamanhos de tela e orientações.
- **Conectividade Independente**: Funciona offline ou em redes instáveis, graças ao Service Worker.
- **App-like**: Proporciona uma experiência semelhante a um aplicativo nativo, com navegação fluida e recursos de tela cheia.
- **Segurança**: Restrito ao protocolo HTTPS.
- **Atualizações**: Usa um Service Worker para cache e atualizações em segundo plano.

## Exemplos Práticos
### 1. Adicionando um Manifesto
O Manifesto é um arquivo JSON que fornece informações essenciais sobre o seu PWA, como o nome, ícones e cores. Crie um arquivo `manifest.json`:
```json
{
  "name": "Meu PWA Incrível",
  "short_name": "PWA",
  "description": "Um exemplo de Progressive Web App.",
  "start_url": "/index.html",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#000000",
  "icons": [
    {
      "src": "icons/icon-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icons/icon-512x512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```
Adicione o manifesto ao seu `index.html`:
```html
<link rel="manifest" href="/manifest.json">
```
### 2. Configurando um Service Worker
O Service Worker permite que você gerencie o cache e as solicitações de rede. Crie um arquivo `service-worker.js`:
```js
const CACHE_NAME = 'my-cache-v1';
const urlsToCache = [
  '/',
  '/styles/main.css',
  '/script/main.js',
  '/icons/icon-192x192.png',
  '/icons/icon-512x512.png'
];

self.addEventListener('install', event => {
  event.waitUntil(
    caches.open(CACHE_NAME)
      .then(cache => cache.addAll(urlsToCache))
  );
});

self.addEventListener('fetch', event => {
  event.respondWith(
    caches.match(event.request)
      .then(response => response || fetch(event.request))
  );
});
```
> Fique atento com os caminhos dos **seus** arquivos!

e por fim, registre o Service Worker na `ìndex.html`:
```html
<script>
  if ('serviceWorker' in navigator) {
    window.addEventListener('load', () => {
      navigator.serviceWorker.register('/service-worker.js')
        .then(registration => {
          console.log('ServiceWorker registrado com sucesso:', registration);
        })
        .catch(error => {
          console.log('Falha ao registrar o ServiceWorker:', error);
        });
    });
  }
</script>
```
### 3. Testando Offline
Para garantir que sua aplicação funcione offline, desconecte a internet e veja se a aplicação ainda carrega. O Service Worker deve servir os arquivos do cache.

## PWAs com Frameworks

### Angular
Angular facilita a criação de PWAs com o Angular CLI. Para adicionar suporte a PWA em um projeto Angular, use o seguinte comando:
```bash
ng add @angular/pwa
```
Este comando adiciona automaticamente o Manifesto e o Service Worker ao seu projeto. O Angular Service Worker é configurado no arquivo `gsw-config.json`. Aqui está um exemplo básico de configuração:
```json
{
  "index": "/index.html",
  "assetGroups": [
    {
      "name": "app",
      "installMode": "prefetch",
      "resources": {
        "files": [
          "/favicon.ico",
          "/index.html",
          "/*.(js|css|png|jpg|woff2|woff|ttf|eot)"
        ]
      }
    }
  ]
}
```
### React
Para criar um PWA com React, você pode usar o create-react-app, que já inclui suporte para PWAs. Crie um projeto React e ative o Service Worker:
```bash
npx create-react-app my-pwa
cd my-pwa
```
No arquivo `src/index.js`, substitua o `serviceWorker.unregister()` por `serviceWorker.register()`:
```js
import * as serviceWorker from './serviceWorker';

serviceWorker.register();
```

### Vue.js
Para adicionar suporte a PWA em um projeto Vue.js, use o plugin `@vue/cli-plugin-pwa`:
```bash
vue add pwa
```
Isso adicionará um `manifest.json` e um Service Worker ao seu projeto. A configuração do Service Worker pode ser encontrada em `vue.config.js`:
```js
module.exports = {
  pwa: {
    name: 'Meu PWA Vue',
    themeColor: '#4DBA87',
    msTileColor: '#000000',
    manifestOptions: {
      background_color: '#ffffff'
    }
  }
}
```

Com essas informações e exemplos, você está pronto para explorar o mundo dos PWAs e criar aplicações web que oferecem uma experiência de usuário incrivelmente rica e envolvente.

Até a próxima, devs! 🚀