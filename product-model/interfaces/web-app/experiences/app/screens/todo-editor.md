---
{
  "entities": [
    {
      "entity": "todo",
      "shows": [
        "Title",
        "Deadline"
      ],
      "collects": [
        "Title",
        "Description",
        "Priority",
        "Project",
        "Section",
        "Deadline",
        "Repeat",
        "Pinned"
      ]
    },
    {
      "entity": "project",
      "shows": [
        "Name"
      ]
    },
    {
      "entity": "section",
      "shows": [
        "Name"
      ]
    },
    {
      "entity": "reminder",
      "shows": [
        "Remind at",
        "Source"
      ],
      "collects": [
        "Remind at"
      ]
    },
    {
      "entity": "subtask",
      "shows": [
        "Title"
      ],
      "collects": [
        "Title"
      ]
    },
    {
      "entity": "comment",
      "shows": [
        "Body",
        "Written at"
      ],
      "collects": [
        "Body"
      ]
    },
    {
      "entity": "attachment",
      "shows": [
        "File name",
        "File type",
        "Size",
        "Uploaded at",
        "File content"
      ]
    },
    {
      "entity": "instance-settings",
      "shows": [
        "Allowed attachment types"
      ]
    },
    {
      "entity": "place",
      "shows": [
        "Name",
        "Address"
      ]
    },
    {
      "entity": "location-reminder",
      "shows": [
        "Trigger",
        "Address"
      ],
      "collects": [
        "Trigger",
        "Address"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/todos.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/todo-attachments.js"
    }
  ]
}
---

# Todo editor

One todo's content, planning details, checklist, comments and attachments.
