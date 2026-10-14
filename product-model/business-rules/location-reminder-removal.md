---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "location-reminder",
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
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/places.py"
    }
  ]
}
---

# A person removes only their own location reminders

Location reminders belong to the person who set them, even on a shared todo.
