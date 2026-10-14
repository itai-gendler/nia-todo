---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses to delete the done todos of a Project and confirms the count",
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
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Completed at"
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
      "text": "The Product permanently deletes the done todos of the project and its subprojects",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "removes",
          "from": "Done"
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
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

# Delete a project's done todos

## Trigger

A project's Done list has grown long.

## Outcome

The completed todos are gone for everyone in the project.
