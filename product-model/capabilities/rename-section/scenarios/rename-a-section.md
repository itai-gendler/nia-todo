---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a new name for a Section",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "changes",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    },
    {
      "text": "The Product saves it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "changes",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project"
        }
      }
    }
  ]
}
---

# Rename a section

## Trigger

A phase gets a better name.

## Outcome

Everyone in the project sees the new name.
