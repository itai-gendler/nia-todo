---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a name and picks a color and an optional icon",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
          "effect": "creates",
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
      "text": "The Product creates the Workspace with its own Inbox project",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
            "Default",
            "Order"
          ]
        },
        {
          "entity": "project",
          "as": "inbox",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
            "Workspace",
            "Inbox",
            "Order"
          ],
          "with": "workspace"
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

# Create a workspace

## Trigger

A person wants to keep work todos apart from private ones.

## Outcome

The new workspace is available with an empty Inbox.
