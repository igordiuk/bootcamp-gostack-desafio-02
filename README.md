<h1 align="center">
  <img alt="Fastfeet" title="Fastfeet" src="https://github.com/Rocketseat/bootcamp-gostack-desafio-02/raw/master/.github/logo.png" width="300px" />
</h1>

<h3 align="center">
  Desafio 2: FastFeet
</h3>

<h3 align="center">
  :warning: Etapa 1/4 do Desafio Final :warning:
</h3>

<blockquote align="center">“Não espere para plantar, apenas tenha paciência para colher”!</blockquote>

<p align="center">
<a href="#rocket-sobre-o-desafio">Sobre o desafio</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
<a href="#um-pouco-sobre-as-ferramentas">Ferramentas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
<a href="#como-instalar-o-projeto-na-sua-máquina">Como Instalar </a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
<a href="#funcionalidades">Funcionalidades</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;


## :rocket: Sobre o desafio
Esse desafio é a primeira parte do Desafio Final que será uma aplicação completa (Back-end, Front-end e Mobile) de uma transportadora fictícia denominada FastFeet.

Nesse primeiro desafio criei algumas funcionalidades básicas que aprendi ao longo das aulas. Ao final da minha jornada terei uma aplicação completa envolvendo back-end, front-end e mobile, que será utilizada para a **certificação do bootcamp**.

## **Um pouco sobre as ferramentas**
Durante a resolução do desafio, utilizei as ferramentas :

- NodeJS
- Yarn
- Express
- Sucrase
- Nodemon
- ESLint
- Prettier
- EditorConfig
- Yup (para validações)
- Docker com imagem do Postgre (opcional)
- Sequelize (PostgreSQL)


## **Como instalar o projeto**
1. Clone o repositório em sua máquina.
2. Instale as dependecias do projeto :&nbsp;&nbsp;&nbsp; `yarn`&nbsp;  ou &nbsp; `npm install`
3. Após finalizar as configurações, execute no seu terminal `yarn dev`

## **Utilizando o Docker**
1. Caso deseje utilizar o docker com a imagem do Postgre, execute no seu terminal `docker run --name fastfeet -e POSTGRESS_PASSWORD=<yourpasswordhere> -p 5432:5432 -d postgres`

## **Configurando o Banco e Dados**
1. Dentro da pasta <code>./src/config</code>, edite o arquivo <strong>database.js</strong> inserindo as credenciais de acesso ao seu banco de dados
2. Para criar as tabelas, no terminal execute: `yarn sequelize db:migrate`
3. Para criar o usuário Administrador da Aplicação, no terminal execute: `yarn sequelize db:seed:all`

## **Funcionalidades**

Abaixo estão descritas as funcionalidades adicionadas a aplicação.

### **1. Autenticação dos Administradores**

Criei a permissão para que um usuário se autentique na aplicação utilizando e-mail e uma senha.

- A autenticação foi feita utilizando JWT.
- Realizei a validação dos dados de entrada com o Yup.
- Administrador tem acesso as rotas da aplicação, podendo gerenciar todos os destinatários.

### **2. Gestão de destinatários**

Criei a permissão para que os destinatários sejam mantidos na aplicação.

- O gerenciamento de destinatários só pode ser feito por administradores autenticados na aplicação.
- Realizei a validação dos dados de entrada com Yup.
- O destinatário não pode se autenticar no sistema, ou seja, não possui uma senha de acesso.
