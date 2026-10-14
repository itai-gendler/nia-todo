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

# Create workspace

A person adds a workspace, such as Work, to group projects by context. It gets its own Inbox.
