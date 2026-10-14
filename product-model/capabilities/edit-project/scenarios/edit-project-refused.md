---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks a parent that sits under the project itself, or moves an Inbox to another workspace",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "changes",
          "facts": [
            "Parent project",
            "Workspace"
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
      "text": "The Product refuses",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": [
            "Inbox",
            "Parent project"
          ]
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

# Make a project its own ancestor or move the Inbox

## Trigger

A person drags a project under its own subproject.

## Outcome

The project stays where it was.
