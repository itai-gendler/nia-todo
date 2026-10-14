---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User tries to delete their default Workspace",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": [
            "Name",
            "Default"
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
      "text": "The Product refuses",
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

# Delete the default workspace

## Trigger

A person tries to remove Personal.

## Outcome

The default workspace stays.
