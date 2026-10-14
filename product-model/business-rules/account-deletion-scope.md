---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "delete-user"
    },
    {
      "type": "entity",
      "id": "todo",
      "effect": "removes"
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

# Deleting an account removes everything it created

The account's workspaces, projects, todos (including those it created in other people's shared projects), comments, attachments, places and API keys go with it.
