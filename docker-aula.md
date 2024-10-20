---
author: Humberto (op3n)
pubDatetime: 2024-10-17T05:00:00.000Z
modDatetime: 2024-10-17T05:00:00.000Z
title: Como usar o docker no Linux? (Aula 3 - Bash Script)
slug: docker-iniciantes
featured: false
draft: false
tags:
 - backend
 - iniciantes
 - minicurso
 - basico
description: Nessa aula, você aí, vai aprender a usar containers docker, e melhor, no conforto do seu Linux (Debian Based)
---

# Starting the computer... or no, right?
---

Olá meus amigos devs, tudo top com vocês? Quem tá vivo sempre aparece, e depois de uma semana sem fazer artigo, tô de volta! Hoje eu vou falar sobre uma das maravilhas do mundo Linux! Os containers Docker, lá tu consegue desde hospedar uma Google Cloud (nextcloud), ao apse de rodar macos no seu computador, como, eu poderia até falar, mas não quero ser preso hoje não kkk

# Uhhh, error? Oh it's only the grub.
---

Bem, brincadeiras a parte, vamos começar com a teoria, mas como docker não tem lá muita teoria, relaxa que eu vou torturar você pouco saskklsk. O Docker, é basicamente constituido de:

- Docker Files = "Basicamente, o DockerFile é um arquivo de script que contém comandos para construir uma imagem docker, exemplo: FROM, RUN, COPY e etc..."
- Docker Hub = "Em Linux, especificamente APT, você aprendeu que nós temos um repositório com varios pacotes .deb, mas você também pode rodar o .deb local, certo? No Docker é exatamente a mesma coisa, ou seja, você tem opção de rodar um docker file do zero, ou apenas rodar usando o Docker Hub, que no caso, é o que você vai aprender aqui, que tal um artigo apenas sobre docker? Em fim..."
- Contêiners = "São basicamente, aonde vão rodar as aplicações docker.... Apenas isso mesmo..."


# What the hell, what is this Black and White screen, oh, it's the terminal!

---

Falei que eu não iria torturar muito vocês em teoria! Sejam bem vindos a... `PARTE PRÁTICA!!`, aproveita pra comemorar enquanto tu não vai ter que lidar com erro de docker file, em fim, continuando, aqui você vai entender como rodar basicamente qualquer sistema usando o docker... Literalmente qualquer sistema, aplicação, tudo!

## Instalando o Docker...

---

Chega de piadas, vamos lá, para instalar o Docker você precisa primeiro, ter uma dominância melhor em Bash, então, recomendo você voltar nas partes 1/2 antes de ir para essa, ou você pode ficar beeeemmmm confuso(a), de qualquer forma, se quiser encarar, boa sorte! Lembrando, esse tutorial é **APENAS** para *Debian Baseds* (Debian, Ubuntu, Pop! OS, Linux Mint, etc..), caso contrário, vocẽ pode ter algum problemas já na primeira parte.
---
Primeiro precisamos atualizar os pacotes e limpar caches, para garantir que nada vai dar errado, então abra seu terminal e digite os seguintes comandos: 

`sudo apt clean` - Remove o "cache" de seus repositórios apt, dando mais tranquilidade para remover conflitos.

```bash
Entendendo o comando:

sudo - rodar como root (Administrador)
apt - Gestor de repositórios
clean - "Limpar Cache"

``` 


Em seguida, já podemos realizar a instalação do Docker, mas antes, para certificarmos, vamos atualizar os repositórios para que não tenhamos nenhum erro inexperado.

`sudo apt update && sudo apt upgrade -y`

```bash
Entendendo o comando:

sudo - Rodar como root (Administrador)
apt - Gestor de repositórios
update - Atualizar os repositórios

&& - Conector, aprendemos nas aulas anteriores a usa-lo

sudo - Rodar como root (novamente)
apt - Gestor de repositórios
upgrade - Atualizar pacotes do sistema (Ou o próprio sistema)
-y :-: Confirmar a operação, similar a: "Yes, Sure, Sim, Concordo, Agree" 
```

---

Perfeito! Agora você já tem tudo certo para instalar o Docker em sua máquina, para isso, utilize o comando a baixo:

`sudo apt install docker.io -y` - Instala o docker.io (Opção 1)

Caso dê erro, pode ser que seja a sua distro, por isso tente a **Opção 2**

`sudo apt install docker -y` (Opção 2)

Se ainda assim dê erro, tente a última opção:

`sudo apt install docker-ce -y`

Caso ainda assim tenha dado erro, tenho duas hipoteses:

- 1° = "Você não seguiu os passos corretamente, e por isso, deu errado..."
- 2° = "Sua distro está muito desatualizada, e os repositórios estão conflitantes, solução: Tente instalar uma nova iso do sistema"
- 3° = "Sua distro não é Debian Based..."

---

## Instalado!! Graças a, em fim, quem você acredite...

Bom, não estamos falando de religião, mas de qualquer forma, agora, parabéns! Você tem o Docker instalado com sucesso na sua máquina, e agora, vou te ensinar a como usar essa ferramenta tão poderosa! Mas, calminha ae que preciso instalar na minha maquina virtual, espera um pouquin ai, só um pouco... Mais um pouco.. pronto!
---

Prontinho, antes de começarmos, mais uma verificação porque Docker gosta de dar um errinho safado kkkk


`sudo service docker restart`

```bash
Entendendo o comando:

sudo - Executar como root (Administrador)
service - Ferramenta de serviços (systemctl)
docker - Serviço (docker.service)
restart - Ação, no caso reiniciar.
```


---

Perfeito! Agora sim, seu docker está quase ant-erros, agora, vamos aos comandos básicos.

Quando você quer criar um container usando o [Docker Hub](https://hub.docker.com "Docker Hub - Site Oficial"), aí você vai encontrar basicamente, todas as imagens docker.


1° Passo - Pesquisar pelo que quer (E.x: Arch Linux)
(Colocar imagem aqui)

2° Passo - Copiar o comando que está lá dentro (E.x: Arch Linux)
(Colocar imagem aqui)

3° Passo - Aguardar dar o push, o que pode demorar de Muito, a bastante!

4° Passo - Simplesmente rodar a maquina! Yei!
(Colocar imagem aqui)


Para isso, basta você rodar o comando:
```bash
docker run -it archlinux /bin/bash


Compreendendo o comando:

docker - Ferramenta
run - Rodar
it - "Esse/Essa"
archlinux - Nome da imagem
/bin/bash - O shell, no caso simplificando, o terminal.
```


# The computer turned on.. Finally!

Parabéns! Você aprendeu nesse artigo o básico de Docker, e como em todo artigo que eu faço, aqui eu te dei o básico, e enquanto eu não lanço uma continuação, tente pesquisar na internet como rodar o Docker, mais imagens e tire suas dúvidas, afinal, você está usando o seu aliado (internet), para acessar isso não é verdade askdaksjd!

---

Obrigado mais uma vez pela sua leitura, e espero ter te ajudado em algo! Vlw, flw e fuis!
