---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "place",
      "effect": "reads"
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

# Only its owner sees a place

Saved places are private.
