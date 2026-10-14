---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reminder"
    },
    {
      "type": "entity",
      "id": "location-reminder"
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

# Reminders and location reminders are personal

On a shared todo each person has their own reminder and location reminder; others never see or receive them.
