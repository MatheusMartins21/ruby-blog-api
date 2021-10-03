# Blog API (By: Matheus Martins)

## Projeto criado com:
<code>rails new blog-api --api</code>

Este projeto tem como objetivo apresentar os estudos da linguagem Ruby com a criação de uma API de um blog conforme os objetivos abaixo:
- Rota para os "posts" do meu blog
- Rota para os comentários dos "posts" do meu blog
- Apenas a Rota de "posts" podem utilizar os métodos PATCH/PUT

Para executar o projeto você deve ter configurado todo o ambiente para o Ruby on Rails e utilizar o comando <code>bundle</code> para a instalação das dependências dentro do projeto.

### Scaffold
<code>rails g scaffold Post title:string description:string content:string author:string</code>

<code>rails g scaffold Comment content:string author:string email:string Post:references</code>

### Dados:
#### /posts
<code>
{
  "id": 1,
  "title": "Primeiro Post",
  "description": "Meu primeiro post =)",
  "content": "Olá mundo!",
  "author": "Matheus"
},
{
  "id": 2,
  "title": "Segundo Post",
  "description": "Meu segundo post =)",
  "content": "Olá mundo!",
  "author": "Matheus Martins"
},
{
  "id": 4,
  "title": "Terceiro Post",
  "description": "Meu terceiro post =)",
  "content": "Olá mundo!",
  "author": "Matheus Martins"
}
</code>

#### /comments
<code>
{
  "id": 1,
  "content": "Post legal =D",
  "author": "Matheus",
  "email": "teste@email.com.br",
  "Post_id": 1,
  "created_at": "2021-10-03T22:40:28.525Z",
  "updated_at": "2021-10-03T22:40:28.525Z"
}
</code>