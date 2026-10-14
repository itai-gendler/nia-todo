---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens In progress or Done",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::status-lists"
        }
      }
    },
    {
      "text": "The Product lists the todos in that status",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Project",
            "Completed at"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::status-lists"
        }
      }
    }
  ]
}
---

# Open the In progress or Done list

## Trigger

A person reviews what they finished this week.

## Outcome

The person sees every todo in that status.
