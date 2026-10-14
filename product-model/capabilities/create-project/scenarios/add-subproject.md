---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User creates a project and picks one of their projects in the same workspace as its parent",
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
            "Workspace",
            "Parent project"
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
      "text": "The Product creates the Project under its parent",
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

# Create a subproject

## Trigger

A person splits Renovation into Kitchen and Bathroom.

## Outcome

The subproject shows under its parent.
