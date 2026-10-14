---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "create-user"
    },
    {
      "type": "entity",
      "id": "workspace",
      "facts": [
        "Default"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    }
  ]
}
---

# New accounts start with a Personal workspace and starter projects

An account the administrator creates starts with the Personal workspace holding an Inbox and the projects Personal, Work and Shopping.
