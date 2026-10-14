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
      "target": "api/migrations/048_add_todo_subtasks.sql"
    }
  ]
}
---

# Subtask

One step on a todo's checklist.

## Information kept

- **Title** — the step, up to 500 characters
- **Order** — where it sits on the checklist

## States

### Open

Not yet checked off.

### Done

Checked off.
