# APITask

API mínima de lista de tarefas (to-do) com **Minimal APIs do .NET 6** e banco em memória do Entity Framework Core.

> Projeto de estudo (abril/2022), feito para experimentar as Minimal APIs logo que saíram no .NET 6. Todo o código está em um único `Program.cs`.

## Endpoints

| Método | Rota | Descrição |
| --- | --- | --- |
| GET | `/tasks` | Lista todas as tarefas |
| GET | `/tasks/completed` | Lista só as concluídas |
| GET | `/tasks/{id}` | Busca uma tarefa |
| POST | `/tasks` | Cria uma tarefa |
| PUT | `/tasks/{id}` | Atualiza nome e status |
| DELETE | `/tasks/{id}` | Remove uma tarefa |
| GET | `/frases` | Busca uma frase aleatória numa API pública externa |

Exemplo de corpo para `POST /tasks`:

```json
{ "name": "Estudar Minimal APIs", "isCompleted": false }
```

## Tecnologias

- .NET 6 / ASP.NET Core Minimal APIs
- Entity Framework Core InMemory (os dados somem ao reiniciar)
- Swashbuckle (Swagger)

## Como executar

Pré-requisito: SDK do .NET 6. Não precisa de banco.

```bash
dotnet run --project ApiTask
```

Depois abra o Swagger em `/swagger`.

---

Feito por **Mikael Francisco** · [Portfólio](https://mikaelfrancisco.vercel.app) · [LinkedIn](https://www.linkedin.com/in/mikael-francisco-a4300b180)
