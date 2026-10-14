---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the name, color or icon of a Workspace",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
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
          "place": "web-app::app::workspace-editor"
        }
      }
    },
    {
      "text": "The Product saves it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
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
          "place": "web-app::app::workspace-editor"
        }
      }
    }
  ]
}
---

# Edit a workspace

## Trigger

A person renames Work to Office.

## Outcome

The workspace shows its new name, color and icon on every device.

## Edge cases

- A name the person already uses for another workspace is refused.
