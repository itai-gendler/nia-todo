---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "todo",
      "facts": [
        "Repeat",
        "Deadline"
      ]
    },
    {
      "type": "capability",
      "id": "create-todo"
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

# A repeating todo needs a deadline

The deadline is the starting point of the repeat; a todo without one cannot repeat.
