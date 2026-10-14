---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reminder",
      "effect": "changes",
      "facts": [
        "Remind at",
        "Source"
      ]
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

# A person moves only their own reminders

Changing a deadline moves only the reminders of the person who changed it.
