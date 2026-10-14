---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User names a new Section in a Project",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "section",
          "effect": "creates",
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
      "text": "The Product adds it after the existing sections",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "section",
          "effect": "creates",
          "facts": [
            "Name",
            "Order"
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

# Add a section

## Trigger

A person groups a project's todos into phases.

## Outcome

The section appears for everyone in the project.
