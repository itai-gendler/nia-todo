---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "workspace",
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
      ],
      "when": [
        {
          "fact": "Default",
          "is": "No"
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

# Only its owner deletes a workspace, and never the default one

A person deletes their own workspaces except the default Personal workspace.
