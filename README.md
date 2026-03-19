# 📝 ToDo List API

API REST para gerenciamento de tarefas (To-Do List) desenvolvida com Spring Boot, aplicando boas práticas como arquitetura em camadas, validação de dados, tratamento de erros e autenticação com JWT via Spring Security.

## 🚀 Tecnologias

* Java 21
* Spring Boot
* Spring Web
* Spring Data JPA
* Spring Security
* JWT
* Hibernate
* Maven

## 📌 Funcionalidades

### 👤 Usuários

* Cadastro de usuários
* Autenticação com JWT

### ✅ Tarefas

* Criar tarefa
* Listar tarefas
* Atualizar tarefa
* Deletar tarefa

### 🔎 Filtros

* Filtragem de tarefas por critérios

### ⚠️ Tratamento de erros

* Respostas padronizadas de erro
* Validação de dados

## 📂 Estrutura do projeto

O projeto segue arquitetura em camadas:

* `controller` → Entrada das requisições
* `service` → Regras de negócio
* `repository` → Acesso ao banco
* `user` → Módulo de usuários
* `task` → Módulo de tarefas
* `filter` → Filtros
* `errors` → Tratamento de exceções
* `utils` → Utilitários

## ▶️ Como executar

```bash
# Clonar repositório
git clone https://github.com/seu-usuario/todolist-api.git

# Entrar na pasta
cd todolist-api

# Rodar aplicação
./mvnw spring-boot:run
```

A API estará disponível em:
http://localhost:8080

## 🔐 Autenticação

A API utiliza autenticação via JWT.

1. Faça login
2. Receba o token
3. Envie no header das requisições:

Authorization: Bearer {token}

## 🔍 Exemplos de endpoints

| Método | Endpoint    | Descrição        |
| ------ | ----------- | ---------------- |
| POST   | /auth/login | Login usuário    |
| POST   | /users      | Criar usuário    |
| GET    | /tasks      | Listar tarefas   |
| POST   | /tasks      | Criar tarefa     |
| PUT    | /tasks/{id} | Atualizar tarefa |
| DELETE | /tasks/{id} | Remover tarefa   |

## 📚 Objetivo

Projeto desenvolvido para praticar construção de APIs REST com Spring Boot, segurança com JWT e boas práticas de organização de código.

## 💡 Melhorias futuras

* Paginação
* Swagger (documentação)
* Testes automatizados
* Deploy em cloud

## 📄 Licença

Projeto para fins de estudo.
