---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User deletes a Section and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "reads",
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
      "text": "The Product moves the section's todos to Unsorted and deletes the section",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Section"
          ]
        },
        {
          "entity": "section",
          "effect": "removes"
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

# Delete a section

## Trigger

A phase is no longer needed.

## Outcome

The section is gone; its todos remain in the project under Unsorted.
