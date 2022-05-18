# Introdução ao Git e GitHub usando terminal Linux
### Para preparar o ambiente de desenvolvimento local é preciso alguns passos antes de iniciar o git.
O Git é um sistema de versionamento de controle distribuido
## 1º fazer o Download do Git
 https://git-scm.com/downloads
## 2º Gerar par de chaves local para poder usar o repositório remoto
  $ ssh-keygen -t -C <email do GitHub>
### entrar na pasta das chaves
  $ cd / .ssh/
### listar as chaves
  $ ls
##### o resultado será dois id_<valor>(privado) e um id_<valor>.pub (publico)
### visualizar o conteúdo do id_<valor>.pub copiar (obs deve copiar da chave pública)
  $ cat id_<valor>.pub 
### abrir na aba do perfil e selecionar o Setting > Access > SSH and GPG keys
##### clicar em ssh key, dar um titulo e colar a chave no espaço key.
### Inicializar o SSH agent
  $ eval $(ssh-agent -s)
##### mostratá o agent pid<valor>
### Entregar a chave SSH privada para o agent
  $ ssh-add id_<valor>
##### mostrará identify added: id_<valor> (email github) // concluido com sucesso
## 3º Inicializar o Git em um repositorioGit local
  $ git init
### configurar o usuário e email, lembrando que deve ser igual ao do GitHub para na hora de fazer o commit o usuario seja sua conta pessoal do github
  $ git config --global user.name "usuário github"
  $ git config --global user.email "email do github"
## 4.1º clonar um repositório do GitHub no seu ambiente de desenvolvimento local
##### na pasta tem um botão verde com o nome code, lá tem um link https, click em copiar, e vá para a o repositório local pelo terminal
  $ git clone "link url https......"
## 4.2º criar um diretório no repositório para criar arquivos editáveis
#### criar um diretório
  $ mkdir LivroDeReceitas
#### criar um arquivo dentro do diretório criado anteriormente
  ~LivroDeReceitas$ echo "Lazanha" > READMI.md
## Logar no repositorio remoto
  
  
  

