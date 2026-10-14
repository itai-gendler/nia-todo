---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reminder",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "owns",
          "entity": "user"
        }
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

# A person sets only their own reminders

Reminders belong to the person who set them, even on a shared todo.
