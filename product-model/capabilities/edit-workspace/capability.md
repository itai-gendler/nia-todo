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

# Edit workspace

A person renames a workspace or changes its color or icon. Changing workspaces needs a connection.
