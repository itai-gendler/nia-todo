---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reminder",
      "effect": "removes"
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

# A person removes only their own reminders

Removing a reminder never touches another member's.
