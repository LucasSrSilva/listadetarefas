# Lista de Tarefas

[Backend](https://github.com/LucasSrSilva/listadetarefas-nestjs)

[Frontend](https://github.com/LucasSrSilva/listadetarefas-react)

[Deploy Backend](https://listadetarefas-nestjs.onrender.com)

[Deploy Frontend](https://listadetarefas-react-six.vercel.app/)

# Back-end em NestJS

Este projeto consiste no desenvolvimento de um back-end utilizando NestJS e NPM para gerenciamento de dependências. O sistema foi projetado para ser seguro, escalável e com suporte a diferentes ambientes de execução.

## Tecnologias Utilizadas

- **NestJS**: Framework Node.js para construção de aplicações server-side.
- **NPM**: Gerenciador de pacotes do Node.js.
- **TypeORM**: ORM para interação com o banco de dados.
- **MySQL**: Banco de dados utilizado no ambiente de desenvolvimento.
- **SQLite**: Banco de dados utilizado para testes.
- **PostgreSQL**: Banco de dados utilizado para o deploy em produção.
- **bcrypt**: Biblioteca para hashing seguro de senhas.
- **Passport**: Biblioteca de autenticação.
  - `passport-local`: Estratégia de autenticação local.
  - `jwt-passport`: Autenticação baseada em JWT.
- **JWT (JSON Web Token)**: Gerenciamento de autenticação através de tokens.
- **Supertest**: Biblioteca para testes end-to-end (e2e).
- **Swagger-UI**: Interface para documentação da API.

## Configuração de Ambientes

- **Ambiente de Desenvolvimento**: Utiliza MySQL para armazenamento de dados.
- **Ambiente de Testes**: Utiliza SQLite para testes mais rápidos e simplificados.
- **Produção**: Utiliza PostgreSQL para maior escalabilidade e performance.

## Segurança

A segurança dos usuários é uma prioridade no projeto. Para isso, as senhas são hashadas com `bcrypt`, garantindo que elas nunca sejam armazenadas em texto simples. O sistema de autenticação foi implementado com `passport-local` e `jwt-passport`, utilizando Tokens JWT para gerenciar as sessões de usuários. A chave secreta para assinatura dos tokens JWT está armazenada em um arquivo `constants.ts`, que protege os tokens gerados na aplicação.

## Testes

Os testes end-to-end (e2e) foram desenvolvidos utilizando a biblioteca **Supertest**, que simula o comportamento real do usuário ao interagir com a API.

## Documentação

A documentação da API foi feita com **Swagger-UI**, permitindo uma interface amigável para explorar as rotas e testar os endpoints diretamente no navegador.

## Deploy

O deploy do projeto foi realizado utilizando a plataforma **Render**, proporcionando um ambiente de produção confiável e escalável.

## Como Executar o Projeto

1. **Clone o repositório**:
    ```bash
    git clone <https://github.com/LucasSrSilva/listadetarefas-nestjs>
    ```
2. **Instale as dependências**:
    ```bash
    npm install
    ```
3. **Configuração do Banco de Dados**:
   Em `app.module` na linha `15` faça alteração de `ProdService` para `DevService`.
   
4. **Executar o projeto em desenvolvimento**:
    ```bash
    npm run start:dev
    ```
5. **Testes e2e**:
    ```bash
    npm run test:e2e
    ```



# Front-end em React

Este projeto consiste no desenvolvimento de um front-end utilizando React e Tailwind CSS, com Yarn para o gerenciamento de dependências. O sistema foi integrado ao back-end através do Axios e implementa várias bibliotecas para otimizar a usabilidade e a interface.

## Tecnologias Utilizadas

- **React**: Biblioteca JavaScript para construção de interfaces de usuário.
- **Tailwind CSS**: Framework utilitário de CSS para estilização rápida e responsiva.
- **Yarn**: Gerenciador de pacotes.
- **Axios**: Biblioteca para fazer requisições HTTP ao back-end.
- **React Router DOM**: Biblioteca para gerenciamento de rotas no React.
- **Phosphor Icons**: Conjunto de ícones personalizáveis.
- **React Spinners**: Biblioteca para exibição de indicadores de carregamento.
- **React Toastify**: Biblioteca para exibição de notificações.

## Autenticação

Foi criado um contexto de autenticação (`LoginContext`) para gerenciar o login de usuários de forma centralizada. Isso permite que a função de login seja acessível em qualquer parte da aplicação, garantindo uma experiência fluida e segura.

## Deploy

O deploy do projeto foi realizado utilizando a plataforma **Vercel**, proporcionando uma entrega rápida e eficiente para o ambiente de produção.

## Como Executar o Projeto

1. **Clone o repositório**:
    ```bash
    git clone <https://github.com/LucasSrSilva/listadetarefas-react>
    ```
2. **Instale as dependências**:
    ```bash
    yarn install
    ```
3. **Conexão com o backend**:
   Para conexão com o deploy no render, utilize: `https://listadetarefas-nestjs.onrender.com` caso deseja conectar com o back-end rodando em sua maquina utilize `localhost:4000`
4. **Executar o projeto em desenvolvimento**:
    ```bash
    yarn start
    ```



