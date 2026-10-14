---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "todo",
      "facts": [
        "Title",
        "Description"
      ]
    },
    {
      "type": "entity",
      "id": "subtask",
      "facts": [
        "Title"
      ]
    },
    {
      "type": "entity",
      "id": "comment",
      "facts": [
        "Body"
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

# Todos, subtasks and comments have length limits

A todo title has up to 500 characters and its description up to 50,000; a subtask up to 500 with at most 100 per todo; a comment between 1 and 5,000.
