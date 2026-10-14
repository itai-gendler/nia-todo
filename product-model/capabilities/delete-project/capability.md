---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "projects",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/projects.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/projects.js"
    }
  ]
}
---

# Delete project

The owner deletes a project together with its subprojects and their sections. Their todos are kept: each moves to the Inbox of the person who created it. The Inbox cannot be deleted.
