---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "place",
      "effect": "changes"
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
      "target": "api/routers/places.py"
    }
  ]
}
---

# Only its owner edits a place

A person edits only their own places.
