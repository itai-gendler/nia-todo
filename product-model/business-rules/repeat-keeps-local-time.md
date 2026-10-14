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
      "id": "complete-todo"
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

# A repeat keeps the same local time and the nearest valid day

Repeats follow the person's time zone: across daylight-saving changes the time of day stays, a time that does not exist moves to the next valid minute, and a monthly or yearly repeat on a day the month lacks falls on its last day.
