
# 📌 API de Tarefas - Minimal API com .NET 8

Este projeto é uma **Minimal API** criada com **.NET 8** que fornece um CRUD básico para gerenciamento de tarefas, utilizando um banco de dados em memória (**InMemoryDatabase**) com **Entity Framework Core**.

---

## 🚀 Funcionalidades

- ✅ Listar todas as tarefas
- ✅ Listar uma tarefa por ID
- ✅ Listar tarefas concluídas
- ✅ Criar uma nova tarefa
- ✅ Atualizar uma tarefa existente
- ✅ Remover uma tarefa
- ✅ Buscar frase aleatória do personagem Ron Swanson via API externa
- ✅ Endpoint de teste: "Olá mundo"

---

## 🗂️ Endpoints

| Método | Rota                     | Descrição                               |
| ------ | ------------------------ | --------------------------------------- |
| GET    | `/`                      | Retorna uma mensagem de "Olá mundo"     |
| GET    | `/frases`                | Retorna uma frase aleatória do Ron Swanson |
| GET    | `/tarefas`               | Lista todas as tarefas                  |
| GET    | `/tarefas/{id}`          | Retorna uma tarefa pelo ID              |
| GET    | `/tarefas/concluida`     | Lista todas as tarefas concluídas       |
| POST   | `/tarefas`               | Cria uma nova tarefa                    |
| PUT    | `/tarefas/{id}`          | Atualiza uma tarefa existente           |
| DELETE | `/tarefas/{id}`          | Remove uma tarefa pelo ID               |

---

## 🔧 Exemplo de Tarefa (JSON)

```json
{
  "id": 1,
  "nome": "Estudar .NET 8",
  "isConcluida": false
}
```

---

## 🛠️ Tecnologias e Bibliotecas

- [.NET 8](https://dotnet.microsoft.com/en-us/download/dotnet/8.0)
- [Entity Framework Core InMemory](https://learn.microsoft.com/ef/core/providers/in-memory/)
- [Swagger / Swashbuckle](https://github.com/domaindrivendev/Swashbuckle.AspNetCore)
- [HttpClient](https://learn.microsoft.com/dotnet/api/system.net.http.httpclient) para consumir API externa

---

## ▶️ Como Executar

1. **Clone o repositório:**
```bash
git clone <URL-do-repositorio>
```

2. **Entre na pasta do projeto:**
```bash
cd ApiTarefas
```

3. **Execute a aplicação:**
```bash
dotnet run
```

4. **Acesse o Swagger UI para explorar e testar os endpoints:**
```
https://localhost:{porta}/swagger
```

---

## 🧩 Possíveis Melhorias

- Persistência com banco de dados real (ex: SQL Server, PostgreSQL).
- Implementar autenticação e autorização.
- Adicionar testes unitários e de integração.
- Implementar DTOs para entrada e saída de dados.
- Aplicar padrões como Repository e Service Layer.

---

## ❗ Observações

- O banco de dados está em memória, portanto **os dados são perdidos ao reiniciar a aplicação**.
- O endpoint `/frases` consome uma API pública que pode eventualmente estar indisponível.

---

## 🗃️ Recursos Adicionais

- [Documentação oficial do .NET Minimal APIs](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis)
- [Entity Framework Core](https://learn.microsoft.com/ef/core/)
- [API pública de Frases do Ron Swanson](https://ron-swanson-quotes.herokuapp.com/)

