---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "changes",
      "facts": [
        "Display workspace"
      ]
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "holds",
          "entity": "user"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/projects.py"
    }
  ]
}
---

# Only the member chooses where a shared project shows for them

A member's display workspace is their own choice and is invisible to others.
