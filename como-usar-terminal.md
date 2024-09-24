---
author: Humberto (op3n)
pubDatetime: 2024-09-24T05:00:00.000Z
modDatetime: 2024-09-24T05:00:00.000Z
title: Como usar o terminal? (Iniciantes)
slug: terminal-introducao
featured: false
draft: false
tags:
 - backend
 - iniciantes
 - minicurso
 - basico
description: Aqui, você vai aprender como usar o terminal, aquela ferramenta que praticamente ninguém olha, mas é seu maior aliado!
---



# Linux: "Do início ao fim, tudo o que você precisa saber."

Olá, meu amigo dev, tudo bem? Eu me chamo Humberto, e estou aqui para te ensinar um pouco sobre o mundo Linux, te mostrar a tal "liberdade" que tanto dizem que o Linux tem, contar um pouco sobre a história dele e, principalmente, mostrar que, diferente do que dizem, o Linux é fácil de usar, simples, personalizável e ainda mais leve e seguro.

## Tópico 1: A História

Lá em 1990, nosso amigo Linus Torvalds, um estudante finlandês de ciência da computação, teve uma ideia absurdamente ambiciosa: criar seu próprio sistema operacional. Pode parecer loucura, mas naquela época, os sistemas operacionais eram muito caros, como o Unix, e, ao mesmo tempo, muito limitados, como o MS-DOS.

Ele queria um sistema baseado em Unix, que fosse acessível para todos. Começou como um projeto pessoal, um hobby sem muitas pretensões, e postou num grupo da "Usenet" algo como: "Estou criando um sistema operacional gratuito, apenas como hobby, não será grande e profissional como o GNU".

Esse sisteminha, que ele dizia ser nada e apenas um hobby, virou um kernel, que, em resumo, é a parte central do sistema operacional. Torvalds usou muitos programas do projeto GNU, que estava sendo criado pela FST (Free Software Foundation).

O Linux rapidamente ficou popular entre programadores e entusiastas de computação, já que era de graça, flexível e adaptável. A comunidade de código aberto (open source) começou a participar ativamente, deixando o sistema cada vez melhor. O nome Linux é a junção de Linus e Unix. A combinação entre Linus, Unix e ferramentas GNU se tornou o GNU/Linux.

Após alguns anos, muitas distros surgiram, como o Debian, Red Hat, Slackware e, mais tarde, o Ubuntu.

Hoje, ele é um sistema indispensável, tanto para servidores, por causa de sua alta adaptação e performance, quanto para computadores pessoais. Muitas pessoas o utilizam, como eu, que uso Pop!_OS há algum tempo!

### Subtópico 1.2: O que diabos é distro? O que é Pop!_OS?

O Pop!_OS é uma distro Linux (distribuição Linux), desenvolvida pela empresa System76. Uma distro é basicamente um sistema operacional que usa o Kernel Linux. E o Kernel, por sua vez, é nada mais nada menos que o núcleo do sistema. Uma analogia que gosto de usar é que ele é como a API entre o seu hardware e o seu software!

As distros podem ser classificadas como distros Linux e distros baseadas em outras distros. Por exemplo, o Pop!_OS é baseado em diversas distros.

Especificando, o Pop!_OS é baseado no Ubuntu, o Ubuntu, por sua vez, é baseado no Debian, que, por sua vez, é baseado no Linux. Em resumo, toda distro é baseada em Linux, mas ela provavelmente usou outra distro como núcleo, que também foi baseada em Linux!

## Tópico 2: Ok, distro, kernel, história... bla bla bla... Eu quero mesmo é saber na prática!

Bem, seja bem-vindo à parte prática! A primeira coisa é escolher qual distro você quer rodar. Vou deixar abaixo algumas recomendações para iniciantes:

- **Linux Mint**: O Linux Mint, baseado no Ubuntu, tem uma interface muito parecida com o Windows e ferramentas que eliminam o uso constante e desnecessário do terminal. Acho que você vai gostar!

- **Ubuntu**: Se quer entrar já com o pé esquerdo (literalmente), você pode começar com o Ubuntu. É um sistema bonito, bem diferente do Windows, e completo, sendo o sistema mais popular no mercado Linux, tanto para servidores (Ubuntu Server) quanto em desktops (Ubuntu Desktop).

Agora que você já sabe as opções, vá no site oficial da distro, baixe a ISO (que é 100% de graça) e escolha se vai rodar numa VM (Virtual Machine / Máquina Virtual) ou num PC normal.

Vou fazer um micro tutorial para cada uma das opções.

### Subtópico 2.1: Instalando numa máquina real

Já vi que se interessou! Primeiro, vamos baixar o Balena Etcher, que você também pode baixar sem nenhum custo. Após isso, basta colocar sua ISO dentro do app, selecionar o pendrive, clicar em "flash", esperar (e muito), e bootar pela sua BIOS o pendrive (pesquise na internet como bootar pelo pendrive no seu notebook/PC). Depois, é só seguir a instalação normalmente.

### Subtópico 2.2: Instalando numa máquina virtual

Não é muito diferente do Windows. Basta pegar a ISO, colocar no VirtualBox ou no VMware e bootar. Depois, é só seguir a instalação normalmente.

## Tópico 3: Vamos para a parte mais difícil (mas esperada!)

Lá vamos nós aprender os comandos básicos do Linux. Primeiro, abra seu terminal, geralmente identificado por um ícone de um retângulo com um "$" dentro dele.

Ao abrir, você verá uma tela preta (ou cinza) e talvez até se sinta um hacker. Mas, na verdade, isso é apenas um compilador como Python ou C++, só que muito mais hardcore e divertido!

### Subtópico 3.1: Executando comandos simples/intermediários

No seu terminal, digite o comando `ls`.  
O comando `ls` lista todos os arquivos e pastas do seu diretório.

No seu terminal, digite o comando `mkdir nome-da-pasta`.  
O comando `mkdir` (Make Directory) cria uma pasta.

No seu terminal, digite o comando `cd nome-da-pasta`.  
Esse comando entra na pasta.

No seu terminal, digite o comando `nano nome-do-arquivo.py/.txt/etc`.  
Esse comando abre o editor de arquivos Nano! Para salvar e fechar, use (CTRL + X), depois digite Y e pressione ENTER.

No seu terminal, digite o comando `cd ..`.  
Esse comando volta um diretório.  
Exemplo:  
Diretório anterior: `/var/www/html`  
Diretório após usar o comando: `/var/www`

No seu terminal, digite o comando `pwd`.  
Ele mostra em qual diretório você está!

No seu terminal, digite o comando `rm -r NOME-DO-ARQUIVO/PASTA`.  
Ele remove o arquivo ou pasta. Aviso importante para usuários novatos:  
**ATENÇÃO: O COMANDO `sudo rm -r /*` DELETA TODO O SEU DIRETÓRIO RAIZ. O SISTEMA FICA INUTILIZADO APÓS ISSO. TOME CUIDADO!**

### Subtópico 3.2: Executando comandos legais e relativamente difíceis!

Por último, digite no seu terminal o comando `whoami`.  
Esse comando mostra em qual usuário você está.

Agora que você compreendeu os comandos básicos para mexer no seu diretório, criar e remover arquivos, etc., vamos para a parte considerada mais difícil. Agora, você vai aprender a atualizar repositórios, entender o que são repositórios, como acessar o usuário `root` (que tem todas as permissões), e, para finalizar com chave de ouro, algumas dicas.

1° Comando: `sudo`.  
O comando `sudo` é um escalador de privilégios. Por exemplo, se na instalação você configurou seu usuário como "sergin", ele não terá muitas permissões. Mas, por padrão, existe o administrador, que é o `root`!

Então, vamos começar com um exemplo básico.

Digite no terminal: `whoami`.  
Repare que ele responde com o seu usuário, que não tem permissão alguma. Agora, para provar isso, digite no terminal: `apt update`.  
Ele irá retornar algo como:

```
Lendo listas de pacotes... Pronto
E: Não foi possível abrir arquivo de trava /var/lib/apt/lists/lock - open (13: Permissão negada)
E: Impossível criar acesso exclusivo ao diretório /var/lib/apt/lists/
W: Problema ao remover o link do ficheiro /var/cache/apt/pkgcache.bin - RemoveCaches (13: Permissão negada)
W: Problema ao remover o link do ficheiro /var/cache/apt/srcpkgcache.bin - RemoveCaches (13: Permissão negada)
```

Agora tente executar: `sudo whoami`.  
Ele vai pedir uma senha (a do seu usuário atual). E não se assuste se parecer que você não está digitando — isso é apenas uma questão de privacidade de algumas distros.

Após pressionar ENTER, repare que o resultado será `root` agora!

Você pode estar se perguntando: "Mas toda vez que eu quiser rodar coisas no root, vou precisar usar esse prefixo?". A resposta é: não! Basta utilizar o comando `sudo su`.

Agora, o terminal ficará assim:

```
humberto@pop-os:~$ whoami
humberto
humberto@pop-os:~$ sudo su
[sudo] senha para humberto: 
root@pop-os:/home/humberto# whoami
root
```

Parabéns! Você aprendeu a lógica do comando `sudo`. E agora, vamos aprender a usar o...

## Tópico 4 ("O gestor de apps... NO TERMINAL!")
Sim, criei um tópico só para esse comando, porque para mim, esse é o comando mais importante de todos!

Nesse tópico, você vai aprender a usar o gestor de pacotes do Debian (apt), que está disponivel em todas as distros baseadas no Debian (Debian, Ubuntu, Pop! OS, Linux Mint, etc...)

---

1° Comando: `sudo apt help`

```Resultado esperado: 
apt 2.4.13 (amd64)
Uso: comando apt [opções]

apt é um gerenciador de pacotes de linha de comando e fornece comandos para
pesquisar e gerenciar, bem como consultar informações sobre pacotes.
Ele fornece a mesma funcionalidade que as ferramentas especializadas do APT,
como apt-get e apt-cache, mas permite opções mais adequadas para
uso interativo por padrão.

Comandos mais utilizados:
  list - listar pacotes com base em nomes de pacotes
  search - pesquisar nas descrições dos pacotes
  show - mostrar detalhes do pacote
  install - instalar pacotes
  reinstall - reinstalar os pacotes
  remove - remover os pacotes
  autoremove - Remove automaticamente todos os pacotes não usados
  update - atualiza a lista de pacotes disponíveis
  upgrade - atualiza o sistema ao instalar/atualizar pacotes
  full-upgrade - atualiza o sistema ao remover/instalar/atualizar pacotes
  edit-sources - edite o ficheiro de informações de origem
  satisfy - satisfazer as strings de dependência

Veja apt(8) para mais informação sobre os comandos disponíveis.
As opções de configuração e sintaxe são detalhadas em apt.conf(5).
Informações sobre como configurar as fontes podem ser encontradas em fontes.list(5).
As escolhas de pacote e versão podem ser expressas via apt_preferences(5).
Detalhes de segurança estão disponíveis em apt-secure(8).
                                   Este APT tem Poderes de Super Vaca.

```
Só que provavelmente em inglês. Aqui tem uma breve descrição, mas você está aqui para aprender na prática. então vamos fazer um teste.

---

2° Comando: `sudo apt install cmatrix -y`
Compreendendo o Comando:

```
sudo - Rodar como root. (Necessario para o apt)
apt - gestor de aplicativos.
install - Ação, no caso, instalar (Obs.. no caso de desinstalar, poderia ser por exemplo `sudo apt remove`)
cmatrix - Nome da aplicação.
`-y` - Confirma que quer prosseguir sem nenhum tipo de interrupção.
```
O comando cmatrix, faz um efeito de matrix em seu terminal, quer testar?

---

3° Comando: `cmatrix`
Sempre ao executar um comando no terminal, não tem um botão de sair ou algo assim, quando é um aplicativo em loop, o único jeito de sair, é dando CTRL + C. Cancelando a ação.
E é desse modo que você vai sair desse comando.

---

4° Comando: `clear`
Apesar, de apenas limpar a tela, achei desnecessario mostrar no topico anterior, não exite em testar!

---

5° Comando: `nyancat`
Bem, vamos ver se aprendeu a usar o comando APT.

Como instalamos o nyancat?
```
A: `sudo apt install nyancat`
B: `apt install nyan cat`
C: `apt install nyancat`
D: `sudo apt instalar nyancat`
```
Se você achou que era a letra D, errou completamente! A resposta correta é a letra A.

Por quê as outras estão incorretas?

```
B: `apt install nyan cat`
1° O apt necessita de permissão sudo (root), o que só por ai, o codigo já não funcionaria.
2° (nyan cat) separados, instala o pacote nyan, e depois cat.

C: `apt install nyancat`
Apenas por não estar em pemissão sudo/root

D: `sudo apt instalar nyancat`
Não existe instalar no apt. Apenas isso em ingles que é install.


Então, instale o comando nyancat usando `sudo apt install nyancat`
E depois rode usando o comando `nyancat`
Para parar a execução, igual como em tudo no terminal, utilize CTRL + C
```

## Tópico 5 ("A finalização")

Parabéns por ter chegado aqui! *Você*, aprendeu como instalar um linux, como abrir o terminal, como instalar pacotes, como listar diretorios, como usar o apt, como escalar privilégios, e dentre muitas outras coisas! Agradeço por ler tudo isso, que é praticamente uma documentação, e agora você está pronto para seguir sozinho esta jornada! Agora que vocẽ entende o basico, você já sabe como se virar.

## Topico EXTRA ("Sugestão de estudos")

Como usar o comando GIT?
Como commitar usando o comando GIT?
Como programar usando o NANO?
