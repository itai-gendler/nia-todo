---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks a due range (today, tomorrow, next days, overdue or no date), projects, priorities and statuses",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::filter"
        }
      }
    },
    {
      "text": "The Product lists the matching todos with their counts",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Priority",
            "Pinned",
            "Deadline",
            "Repeat",
            "Project",
            "Section"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::filter"
        }
      }
    }
  ]
}
---

# Filter todos

## Trigger

A person wants everything high priority due this week.

## Outcome

The person works from the filtered list; Reset clears the filters.
