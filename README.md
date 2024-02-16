# Projeto Integrador II [2INFOs]

## Olá!

Este é o repositório que contém o material de apoio, tutoriais, exemplos e exercícios para a disciplina de Projeto Integrador II do [Curso Técnico em Informática para Internet](https://informatica.araquari.ifc.edu.br/) do [IFC - Campus Araquari](https://araquari.ifc.edu.br).

Este material está em constante desenvolvimento. Portanto, caso tenha algumas sugestões de melhoria e/ou correções, por favor entre em contato comigo por e-mail. Se preferir, faça uma solicitação de contribuição ao projeto.

Como contribuir com um projeto privado:

1. Faça um fork do projeto
2. Clone o projeto para a sua máquina
3. Crie uma branch para a sua contribuição
4. Faça as alterações necessárias
5. Faça um commit das alterações
6. Faça um push das alterações
7. Crie um pull request
8. Aguarde a revisão do pull request
9. Após a revisão, o pull request será aceito ou recusado
10. Caso seja aceito, o pull request será mergeado com a branch principal ou, caso seja recusado, o pull request será fechado e você deverá fazer as alterações necessárias
11. Volte para o passo 4
12. Após o merge, você pode deletar a branch criada

Antes de começar, saiba que além deste material elaborado para o segundo ano do Curso Técnico em Informática (2INFOs), também há um material elaborado para o primeiro ano do curso (1INFOs) e um material elaborado para o terceiro ano do curso (3INFOs).

### Ttrilha do Curso

**[Programação I](https://github.com/ldmfabio/Programacao) :arrow_right: [Professor Fábio Longo de Moura](https://github.com/ldmfabio)**

> _Lógica de Programação usando JavaScript_

**[Desenvolvimento Web II](https://eduardo-da-silva.github.io/aula-desenvolvimento-web/) :arrow_right: [Professor: Eduardo da Silva](https://github.com/eduardo-da-silva)**

> _Desenvolvimento front-end usando framework Vue_

**[Projeto Integrador II](https://github.com/ldmfabio/PRIN2) :arrow_right: [Professor: Fábio Longo de Moura](https://github.com/ldmfabio)**

> _Integração de conteúdos ministrados no primeiro e segundo ano do Curso Técnico em Informática para Internet_

**[Desenvolvimento Web III](https://github.com/marrcandre/django-drf-tutorial) :arrow_right: [Professor: Marco André Lopes Mendes](https://github.com/marrcandre/)**

> _Desenvolvimento back-end usando framework Django_

### **_Bons estudos durante a sua jornada!_**

<br>

## SUMÁRIO

1. Uso do Git
   1. [GitHub](#github)
   2. Git via terminal
2. Uso do venv (Virtual Environment - Ambiente Virtual)
   1. Instalação
   2. Criação de um ambiente virtual
   3. Ativação de um ambiente virtual
   4. Desativação de um ambiente virtual
   5. Exclusão de um ambiente virtual
3. Projeto 1: Cadastro de Pessoas
   1. Modelagem
   2. Criação de um projeto Django
   3. Criação de um app
   4. Criação de um model
   5. Uso do Django Admin
4. Projeto 2: Cadastro de Cidades e Estados
   1. Modelagem
   2. Criação de um projeto Django
   3. Criação de um app
   4. Criação de um model
   5. Relacionamento entre tabelas
   6. Uso do Django Admin
   7. Desafio: Unir o cadastramento de pessoas com o cadastramento de cidades e estados
5. Projeto 3: Cadastro de Filmes
   1. Modelagem
   2. Criação de um projeto Django
   3. Criação de um app
   4. Criação de um model
   5. Relacionamento entre tabelas
   6. Uso do Django Admin
6. Projeto 4: Cadastro de Locações de Filme
   1. Modelagem
   2. Criação de um projeto Django
   3. Criação de um app
   4. Criação de um model
   5. Relacionamento entre tabelas
   6. Uso do Django Admin
   7. Desafio: Unir o cadastramento de pessoas, cidades, estados e filmes com o cadastramento de locações de filmes
7. Projeto 5: Cadastro de Livros
   1. Modelagem
   2. Levantamento de Requisitos (Funcionais e Não-Funcionais)
   3. Criação de um projeto Django
   4. Criação de um app
   5. Criação de um model
   6. Relacionamento entre tabelas
   7. Uso do Django Admin
8. Projeto 6: Vendas de Livros
   1. Modelagem
   2. Criação de um projeto Django
   3. Criação de um app
   4. Criação de um model
   5. Relacionamento entre tabelas
   6. Uso do Django Admin
   7. Desafio: Unir o cadastro de livros com as vendas de livros

# GitHub

O GitHub é uma plataforma de hospedagem de código-fonte e arquivos com controle de versão usando o Git. Ele permite que você e outras pessoas trabalhem juntas em projetos de qualquer lugar. Este é um dos motivos que o GitHub é tão popular entre desenvolvedores. O GitHub é uma ferramenta essencial para quem trabalha com desenvolvimento de software. Ele é usado para armazenar, compartilhar e colaborar em projetos de código aberto.

O acesso ao GitHub é gratuito para projetos tanto de código aberto quanto projetos privados. O GitHub também oferece planos pagos para armazenamento privado e colaboração em equipes.

Primeiramente criamos uma conta no GitHub. Após a criação da conta, podemos criar um repositório. Um repositório é um local onde armazenamos nosso projeto. Podemos criar um repositório público ou privado. No repositório, podemos armazenar arquivos, como códigos-fonte, imagens, documentos, entre outros.

Após a criação do repositório, podemos clonar o repositório para a nossa máquina. Clonar um repositório significa que estamos copiando o repositório do GitHub para a nossa máquina. Podemos clonar o repositório usando o terminal ou uma interface gráfica.

Após clonar o repositório, podemos fazer alterações nos arquivos do repositório. Após fazer as alterações, podemos fazer um commit. Um commit é uma confirmação de que fizemos alterações nos arquivos do repositório. Após fazer um commit, podemos fazer um push. Um push é o envio das alterações feitas no repositório local para o repositório remoto.

# Git via terminal

Não usaremos a interface do VSCode como suporte ao uso do GitHub. Usaremos apenas o terminal para executar os comandos do Git.

## Configuração do Git

Antes de começar a usar o Git, precisamos configurar o Git. Para isso, precisamos informar o nome do usuário e o e-mail. Para isso, usamos os comandos `git config --global user.name "Seu Nome"` e `git config --global user.email "Seu E-mail"`.

```bash
git config --global user.name "Seu Nome"
git config --global user.email "Seu E-mail"
```

> **_Observação:_**<br>
> O uso do --global é para informar que o nome e o e-mail informados serão usados em todos os repositórios. Caso queira informar um nome e um e-mail específico para um repositório, basta remover o `--global`.

Nesse momento inicial você também poderá a sua conta do Git no VSCode, caso ainda não tenha feito isso. Embora não usaremos a interface, talvez em algum momento seja necessário para autenticação. Portanto, clique na imagem similar a um avatar no canto inferior esquerdo do VSCode e clique em `Sign in to GitHub`.

## Criar um repositório

Para criar um repositório, basta acessar o GitHub, navegar até a aba `Repositories` e clicar no botão `New` no canto superior direito da tela. Após clicar no botão, informe o nome do repositório, a descrição do repositório, se o repositório será público ou privado, se o repositório terá um arquivo README.md e se o repositório terá um arquivo .gitignore. Após informar essas informações, clique no botão `Create repository`.

Após criar um repositório, você terá a possibilidade de adicionar arquivos no repositório, usando a interface do próprio GitHub. Contudo, para facilitar a nossa, vida, podemos clonar o repositório usando o terminal e, após, abrir o repositório clonado diretamente no VSCode.

> Lembre-se: O GitHub é uma aplicação que trabalha sob a plataforma que incorpora os recursos de controle de versões do `git` para que possam ser usados colaborativamente. O git é um software de controle de versões, apenas. Outras alternativas ao GitHub, que também usam o `git` são, por exemplo: Bitbucket, GitLab, Gitea...

## Clonar um repositório

Para clonar um repositório, basta acessar o repositório no GitHub, clicar no botão `Code` e copiar o link do repositório. Após copiar o link, abra o terminal e navegue até a pasta onde deseja clonar o repositório. Após navegar até a pasta, execute o comando `git clone link-do-repositorio`.

```bash
git clone link-do-repositorio
```

Após clonar o repositório, você terá uma pasta com o nome do repositório na pasta onde você clonou o repositório.

> Lembrando que, para facilitar, você precisa estar acessando a pasta que deseja clonar o repositório, ou seja, a pasta onde ficarão os arquivos deste repositório. Caso você não saiba alguns comandos básicos para criação de pastas via terminal, aqui estão eles:
> - `cd` - Change Directory: Este comando serve para navegar entre as pastas. Por exemplo, se você está na pasta `Documentos` e deseja acessar a pasta `Projetos`, que está dentro da pasta `Documentos`, basta digitar `cd Projetos`.
> - `mkdir` - Make Directory: Este comando serve para criar uma pasta. Por exemplo, se você está na pasta `Documentos` e deseja criar uma pasta chamada `Projetos`, basta digitar `mkdir Projetos`.
> - `ls` - List: Este comando serve para listar os arquivos e pastas que estão dentro da pasta que você está. Por exemplo, se você está na pasta `Documentos` e deseja listar os arquivos e pastas que estão dentro da pasta `Documentos`, basta digitar `ls`.
> - `pwd` - Print Working Directory: Este comando serve para mostrar o caminho da pasta que você está. Por exemplo, se você está na pasta `Documentos` e deseja saber o caminho da pasta `Documentos`, basta digitar `pwd`.
> - `cd ..` - Change Directory: Este comando serve para voltar uma pasta. Por exemplo, se você está na pasta `Projetos`, que está localizada dentro da pasta `Documentos`, e deseja voltar para a pasta anterior, basta digitar `cd ..`.
> - `cd ~` - Change Directory: Este comando serve para voltar para a pasta raiz. Por exemplo, se você está na pasta `Projetos`, que está localizada dentro da pasta `Documentos`, e deseja voltar para a pasta raiz, basta digitar `cd ~`.

## Gerenciar remote

Após clonar o repositório, você terá um repositório local e um repositório remoto. O repositório remoto é o repositório que está no GitHub. O repositório local é o repositório que está na sua máquina. Para gerenciar o repositório remoto, usamos o comando `git remote`.

```bash
git remote
```

O comando `git remote` lista os repositórios remotos que estão vinculados ao repositório local. O repositório remoto padrão é o `origin`. O `origin` é o repositório que foi clonado. Para adicionar um repositório remoto, usamos o comando `git remote add nome-do-repositorio link-do-repositorio`.

```bash
git remote add nome-do-repositorio link-do-repositorio
```

O comando `git remote add` adiciona um repositório remoto ao repositório local. O `nome-do-repositorio` é o nome do repositório remoto que será adicionado. O `link-do-repositorio` é o link do repositório remoto que será adicionado.

Há também a possibilidade de você querer remover um repositório remoto. Para isso, usamos o comando `git remote remove nome-do-repositorio`.

```bash
git remote remove nome-do-repositorio
```

O comando `git remote remove` remove um repositório remoto do repositório local. O `nome-do-repositorio` é o nome do repositório remoto que será removido. Isso serve para remover o vínculo que existe com o que está no GitHub. O repositório remoto continuará existindo no GitHub, mas o repositório local não terá mais vínculo com o repositório remoto. Isso também não afetará os arquivos que estão no repositório local. Eles permanecerão inalterados, apenas não terão vínculo com o repositório remoto, ou seja, as alterações que forem feitas neste arquivo não afetarão o repositório remoto.

O comando `git remote -v` lista os repositórios remotos que estão vinculados ao repositório local, juntamente com o link do repositório remoto.

```bash
git remote -v
```

## Inicializar repositório local e vincular a um repositório remoto
Há também a possibilidade de você inicializar um repositório local e depois vinculá-lo a um repositório remoto. Para isso, usamos o comando `git init` para inicializar o repositório local e o comando `git remote add nome-do-repositorio link-do-repositorio` para vincular o repositório local ao repositório remoto.

```bash
git init
git remote add nome-do-repositorio link-do-repositorio
```

O comando `git init` inicializa um repositório local. O comando `git remote add` adiciona um repositório remoto ao repositório local. O `nome-do-repositorio` é o nome do repositório remoto que será adicionado. O `link-do-repositorio` é o link do repositório remoto que será adicionado.

## Adicionar arquivos

Após clonar um repositório, ou então inicializar um repositório e adicionar vínculo com um repositório remoto (`git remote add ...`), você poderá adicionar arquivos neste repositório. Esses arquivos novos são os arquivos que você criou e que ainda não estão no repositório remoto.

Para adicionar arquivos, usamos o comando `git add nome-do-arquivo`.

```bash
git add nome-do-arquivo
```

Imagine que você criou o arquivo index.html e deseja adicionar este arquivo no repositório. Para adicionar o arquivo index.html no repositório, basta, portanto, executar o comando `git add index.html`.

O comando `git add` adiciona um arquivo no repositório local. O `nome-do-arquivo` é o nome do arquivo que será adicionado no repositório local.

Há também a possibilidade de você adicionar todos os arquivos que estão na pasta do repositório. Para isso, usamos o comando `git add .`.

```bash
git add .
```

O comando `git add .` adiciona todos os arquivos criados e que estão apenas no repositório local, não tendo ainda vínculo com o repositório remoto.

## Commitar arquivos

Após adicionar os arquivos no repositório, precisamos fazer um commit. Um commit é uma confirmação de que fizemos alterações nos arquivos do repositório local e desejamos refletir essas alterações no repositório remoto. Para fazer um commit, usamos o comando `git commit -m "Mensagem do commit"`.

```bash
git commit -m "Mensagem do commit"
```

O comando `git commit` faz um commit no repositório local. O `-m` é uma flag que informa que a mensagem do commit será informada. A `Mensagem do commit` é a mensagem que será informada no commit.

> **Adote alguns padrões para realizar os seus commits!**

Esses padrões são importantes para que você e outras pessoas que trabalham no projeto possam entender o que foi feito em cada commit. Há algumas formas de padronizar, mas uma das mais comuns é a seguinte:

- `feat`: para novas funcionalidades
- `fix`: para correção de bugs
- `chore`: para alterações no processo de build ou ferramentas auxiliares
- `refactor`: para refatoração do código
- `test`: para adição de testes
- `style`: para alterações que não afetam o código (espaços em branco, formatação, ponto e vírgula, etc)
- `perf`: para melhorias de performance
- `docs`: para alterações na documentação
- `ci`: para alterações em arquivos de configuração de CI
- `build`: para alterações em arquivos de configuração de build

Ou seja, digamos que você possui uma tarefa de adicionar um botão no seu site. Você pode fazer um commit com a mensagem `feat: Adiciona botão de contato`. Isso facilitará a compreensão do que foi feito em cada commit.

Ainda, caso esteja usando as issues do GitHub, você pode fazer referência a uma issue no seu commit. Por exemplo, se você está trabalhando na issue #1, você pode fazer um commit com a mensagem `feat: Adiciona botão de contato. Closes #1`. Isso fará com que a issue seja fechada automaticamente quando o commit for mergeado com a branch principal.

> _Nota: Em breve serão abordadas as Issues e então terá maiores detalhes sobre a sua utilização._

## Pushar arquivos

Após fazer um commit, precisamos fazer um push. Um push é o envio das alterações feitas no repositório local para o repositório remoto. Para fazer um push, usamos o comando `git push nome-do-repositorio nome-da-branch`.

```bash
git push nome-do-repositorio nome-da-branch
```

O comando `git push` faz um push no repositório remoto. O `nome-do-repositorio` é o nome do repositório remoto que será feito o push. O `nome-da-branch` é o nome da branch que será feito o push.

Imagine que, ao adicionar vínculo com um repositório remoto, o seu código foi `git remote add _origin_ link-do-repositorio`. Também considere que, pra já, estamos trabalhando apenas com a branch `master` (_ou main - e isso é muito errado! Já vamos descobrir o porquê_). Portanto, para fazer um push, basta executar o comando `git push origin master`.

Após este comando ser executado, você então estará sincronizando os arquivos do repositório local com o repositório remoto, especificamente na branch `master`.

## Atualizar repositório local

Após fazer um push, precisamos atualizar o repositório local. Para atualizar o repositório local, usamos o comando `git pull nome-do-repositorio nome-da-branch`.

```bash
git pull nome-do-repositorio nome-da-branch
```

