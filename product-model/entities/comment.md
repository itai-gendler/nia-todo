---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/049_add_todo_comments.sql"
    }
  ]
}
---

# Comment

A note someone with access to a todo adds to it, shown with its author and time.

## Information kept

- **Body** — the text, Markdown, 1 to 5,000 characters
- **Written at** — when it was added
- **Edited at** — when its author last changed it
