---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the name, color or icon of a Project they own",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "changes",
          "facts": [
            "Name",
            "Color",
            "Icon"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "The Product saves it for the owner and every member",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "changes",
          "facts": [
            "Name",
            "Color",
            "Icon"
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

# Change a project's details

## Trigger

A person renames a project.

## Outcome

Everyone in the project sees the new details at once.
