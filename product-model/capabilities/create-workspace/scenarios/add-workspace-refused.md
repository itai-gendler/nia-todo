---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters no name, or the name of one of their workspaces",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
          "effect": "creates",
          "facts": [
            "Name"
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
      "text": "The Product refuses and asks for another name",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::workspace-editor"
        }
      }
    }
  ]
}
---

# Create a workspace without a name or with a name in use

## Trigger

A person reuses a workspace name.

## Outcome

No workspace is created.
