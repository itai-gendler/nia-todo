---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "workspaces",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/workspaces.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/workspaces.js"
    }
  ]
}
---

# Delete workspace

A person deletes a workspace other than their default one. Its projects move to the default workspace and its Inbox todos to the default Inbox. Deleting workspaces needs a connection.
