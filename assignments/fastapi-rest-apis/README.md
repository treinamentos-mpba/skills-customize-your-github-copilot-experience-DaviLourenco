# 📘 Atividade: Building REST APIs with FastAPI

## 🎯 Objetivo

Construa uma API REST com FastAPI para gerenciar livros, praticando rotas HTTP, validação de dados com Pydantic e operações CRUD. Ao final, você terá uma API executável localmente e documentada automaticamente.

## 📝 Tarefas

### 🛠️ Criar a Primeira Rota da API

#### Descrição
Crie uma aplicação FastAPI com uma rota inicial e execute o servidor localmente para testar a resposta.

#### Requisitos
O programa concluído deve:

- Criar uma instância de `FastAPI` em `main.py`.
- Implementar uma rota `GET /` que retorne um objeto JSON com uma mensagem.
- Iniciar a aplicação com `uvicorn main:app --reload`.
- Permitir que a documentação interativa seja acessada em `/docs`.


### 🛠️ Criar e Listar Livros com Validação

#### Descrição
Adicione endpoints para criar e listar livros. Use modelos Pydantic para validar os dados recebidos e definir a estrutura das respostas. Os dados podem ficar armazenados em uma lista em memória.

#### Requisitos
O programa concluído deve:

- Definir um modelo de entrada com título e autor não vazios.
- Implementar `POST /books` para validar e criar um livro com um identificador único.
- Retornar o livro criado com status HTTP `201 Created`.
- Implementar `GET /books` para retornar todos os livros como uma lista.
- Retornar status HTTP `422 Unprocessable Entity` quando o corpo enviado for inválido.


### 🛠️ Implementar as Operações CRUD Restantes

#### Descrição
Complete a API permitindo consultar, atualizar e remover um livro pelo identificador. Trate identificadores que não existam na coleção.

#### Requisitos
O programa concluído deve:

- Implementar `GET /books/{book_id}` para retornar um livro específico.
- Implementar `PUT /books/{book_id}` para atualizar o título e o autor de um livro.
- Implementar `DELETE /books/{book_id}` para remover um livro.
- Retornar status HTTP `404 Not Found` quando o identificador não existir.
- Retornar status HTTP `204 No Content` ao remover um livro com sucesso.
- Manter os livros em memória e informar que eles são apagados quando o servidor reinicia.