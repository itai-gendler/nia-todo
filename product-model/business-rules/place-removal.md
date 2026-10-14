---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "place",
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
      "target": "api/routers/places.py"
    }
  ]
}
---

# Only its owner deletes a place

A person deletes only their own places.
