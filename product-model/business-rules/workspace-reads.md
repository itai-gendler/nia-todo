---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "workspace",
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
      "target": "api/routers/workspaces.py"
    }
  ]
}
---

# Only its owner sees a workspace

Workspaces are personal: nobody else sees them, not even members of projects in them.
