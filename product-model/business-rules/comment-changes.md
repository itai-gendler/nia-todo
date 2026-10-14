---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "comment",
      "effect": "changes"
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

# Only its author edits a comment

Nobody edits another person's comment.
