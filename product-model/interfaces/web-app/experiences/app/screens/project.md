---
{
  "entities": [
    {
      "entity": "project",
      "shows": [
        "Name",
        "Color",
        "Icon"
      ]
    },
    {
      "entity": "section",
      "shows": [
        "Name",
        "Order"
      ],
      "collects": [
        "Name",
        "Order"
      ]
    },
    {
      "entity": "todo",
      "shows": [
        "Title",
        "Priority",
        "Pinned",
        "Section",
        "Deadline",
        "Repeat",
        "Completed at"
      ],
      "collects": [
        "Section",
        "Project"
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
      "target": "web/static/js/features/sections.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/section-actions.js"
    }
  ]
}
---

# Project

One project's todos by section, with its overview and the option to show or clear done todos.
