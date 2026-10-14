---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "workspace",
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
      "target": "api/routers/workspaces.py"
    }
  ]
}
---

# Only its owner edits a workspace

A person changes only their own workspaces.
