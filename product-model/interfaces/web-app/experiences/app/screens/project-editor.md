---
{
  "entities": [
    {
      "entity": "project",
      "shows": [
        "Inbox",
        "Parent project",
        "Name"
      ],
      "collects": [
        "Name",
        "Color",
        "Icon",
        "Workspace",
        "Parent project"
      ]
    },
    {
      "entity": "workspace",
      "shows": [
        "Name"
      ]
    },
    {
      "entity": "project-membership",
      "shows": [
        "Invited by",
        "Invited with"
      ],
      "collects": [
        "Display workspace"
      ]
    },
    {
      "entity": "user",
      "shows": [
        "Display name",
        "Username"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/projects.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/project-sharing.js"
    }
  ]
}
---

# Project editor

One project's details and organization, and who it is shared with.
