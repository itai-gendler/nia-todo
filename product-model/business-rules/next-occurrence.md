---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "complete-todo"
    },
    {
      "type": "entity",
      "id": "todo",
      "facts": [
        "Repeat",
        "Deadline",
        "Series"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    }
  ]
}
---

# Completing a repeating todo creates its next occurrence

The next occurrence copies the todo's details with its subtasks unchecked; its deadline is the previous deadline advanced by the repeat, not the completion date, and its reminder moves along. Each occurrence produces at most one next one.

## Rationale

Advancing from the deadline keeps a weekly todo on its weekday even when it is completed late or early.
