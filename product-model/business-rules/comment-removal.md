---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "removes"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "writes",
          "entity": "user"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "todo"
        },
        {
          "verb": "creates",
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

# Only its author or the todo's creator deletes a comment

The person who created a todo may delete any comment on it; others delete only their own.
