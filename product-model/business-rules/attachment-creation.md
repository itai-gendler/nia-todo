---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "attachment",
      "effect": "creates"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "has",
          "entity": "todo"
        },
        {
          "verb": "contains",
          "entity": "project"
        },
        {
          "verb": "owns",
          "entity": "user"
        }
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Attachments enabled",
          "is": "On"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "todo"
        },
        {
          "verb": "contains",
          "entity": "project"
        },
        {
          "verb": "has",
          "entity": "project-membership"
        },
        {
          "verb": "holds",
          "entity": "user"
        }
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Attachments enabled",
          "is": "On"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "todo"
        },
        {
          "verb": "creates",
          "entity": "user"
        }
      ],
      "when": [
        {
          "entity": "instance-settings",
          "fact": "Attachments enabled",
          "is": "On"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/attachments.py"
    }
  ]
}
---

# Whoever can see a todo attaches files to it while attachments are enabled

Uploads are open to everyone with access to the todo, as long as the administrator has attachments enabled.
