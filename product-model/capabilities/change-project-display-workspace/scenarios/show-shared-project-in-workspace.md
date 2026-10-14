---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks one of their workspaces for a Project shared with them",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "project-membership",
          "effect": "changes",
          "facts": [
            "Display workspace"
          ]
        },
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "The Product shows the project in that workspace for this member only",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project-membership",
          "effect": "changes",
          "facts": [
            "Display workspace"
          ]
        },
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    }
  ]
}
---

# Show a shared project in another workspace

## Trigger

A colleague's shared project belongs in the member's Work workspace.

## Outcome

The shared project appears in the chosen workspace for this member.
