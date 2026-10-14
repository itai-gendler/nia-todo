---
{
  "availability": [
    {
      "place": "web-app::administration"
    }
  ],
  "domain": "users",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/pages/admin.js"
    }
  ]
}
---

# Delete user

The administrator deletes an account with its workspaces, projects, todos, places and keys. The account created during first-run setup cannot be deleted.
