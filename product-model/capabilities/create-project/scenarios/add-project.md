---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a name, picks a color and optional icon, and chooses the workspace",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
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
      "text": "The Product creates the Project, owned by the person",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
            "Parent project",
            "Workspace",
            "Inbox",
            "Order"
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

# Create a project

## Trigger

A person starts planning a move.

## Outcome

The project appears in the workspace, ready for todos.
