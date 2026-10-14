---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "push-subscription",
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
      "target": "api/routers/push.py"
    }
  ]
}
---

# Only its owner removes a push subscription

Turning push off affects only the person's own browser.
