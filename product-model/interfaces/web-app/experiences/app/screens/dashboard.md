---
{
  "entities": [
    {
      "entity": "workspace",
      "shows": [
        "Name"
      ]
    },
    {
      "entity": "dashboard-preferences",
      "shows": [
        "Compact display",
        "Group by status",
        "Show Relevant now",
        "Show active projects",
        "Show project widgets",
        "Included projects",
        "Metrics",
        "Relevant now groups",
        "Hide empty groups",
        "Active projects"
      ],
      "collects": [
        "Compact display",
        "Group by status",
        "Show Relevant now",
        "Show active projects",
        "Show project widgets",
        "Included projects",
        "Metrics",
        "Relevant now groups",
        "Hide empty groups",
        "Active projects"
      ]
    },
    {
      "entity": "todo",
      "shows": [
        "Title",
        "Priority",
        "Pinned",
        "Deadline",
        "Repeat",
        "Project",
        "Section"
      ]
    },
    {
      "entity": "project",
      "shows": [
        "Name",
        "Color"
      ]
    },
    {
      "entity": "user",
      "collects": [
        "Dashboard sync"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/app-rendering.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/dashboard-preferences-dialog.js"
    }
  ]
}
---

# Dashboard

The workspace's overview: metric tiles, the Relevant now groups and active projects, shaped by the person's dashboard preferences.
