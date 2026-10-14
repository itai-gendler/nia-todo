---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reminder",
      "facts": [
        "Source",
        "Remind at"
      ]
    },
    {
      "type": "capability",
      "id": "create-todo"
    },
    {
      "type": "capability",
      "id": "edit-todo"
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

# A deadline brings an automatic reminder when the person has a default reminder

When a person with a default reminder gives a todo a deadline and chooses no reminder time, they get a reminder that long before the deadline, and it follows the deadline when it moves. A time the person chooses replaces it and stays put.
