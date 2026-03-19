# 📝 ToDo List API

API REST para gerenciamento de tarefas (To-Do List) desenvolvida com Spring Boot, com foco em boas práticas, validações de negócio e controle de acesso por usuário.

## 🚀 Tecnologias

* Java 21
* Spring Boot
* Spring Web
* Spring Data JPA
* Hibernate
* Maven
* BCrypt (hash de senha)

## 📌 Funcionalidades

### 👤 Usuários

* Cadastro de usuário
* Validação de usuário já existente
* Criptografia de senha com BCrypt

### 🔐 Autenticação

* Autenticação via Basic Auth
* Validação de credenciais no filtro
* Proteção de rotas `/tasks`
* Associação de tarefas ao usuário autenticado

### ✅ Tarefas

* Criar tarefa vinculada ao usuário
* Listar tarefas do usuário
* Atualizar tarefa
* Validação de permissão (usuário só altera suas próprias tarefas)

### ⏰ Regras de negócio

* Data de início e término devem ser maiores que a data atual
* Data de início não pode ser maior que a data de término

### ⚠️ Tratamento de erros

* Retornos com status HTTP apropriados
* Mensagens de erro claras

## 📂 Estrutura do projeto

* `user` → Cadastro de usuários
* `task` → Regras e operações das tarefas
* `filter` → Autenticação e interceptação de requisições
* `errors` → Tratamento de exceções
* `utils` → Funções auxiliares

## ▶️ Como executar

```bash id="t7e9mz"
git clone https://github.com/seu-usuario/todolist-api.git
cd todolist-api
./mvnw spring-boot:run
```

## 🔍 Autenticação (exemplo)

Header da requisição:

```
Authorization: Basic base64(usuario:senha)
```

Exemplo usando curl:

```bash id="v7c4rp"
curl -X GET http://localhost:8080/tasks/ \
-u usuario:senha
```

## 🔍 Endpoints

### Usuários

| Método | Endpoint | Descrição     |
| ------ | -------- | ------------- |
| POST   | /users/  | Criar usuário |

### Tarefas

| Método | Endpoint    | Descrição        |
| ------ | ----------- | ---------------- |
| POST   | /tasks/     | Criar tarefa     |
| GET    | /tasks/     | Listar tarefas   |
| PUT    | /tasks/{id} | Atualizar tarefa |

## 📚 Objetivo

Projeto desenvolvido para praticar construção de APIs REST, autenticação, validação de dados e controle de acesso.

## 💡 Diferenciais

* Autenticação customizada com filtro
* Controle de acesso por usuário
* Criptografia de senha com BCrypt
* Validação de regras de negócio
* Update parcial de entidades

## 📄 Licença

Projeto para fins de estudo.
