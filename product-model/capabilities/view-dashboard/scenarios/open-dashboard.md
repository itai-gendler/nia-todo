---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens the dashboard of a Workspace",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        },
        {
          "entity": "dashboard-preferences",
          "effect": "reads",
          "facts": [
            "Compact display",
            "Group by status",
            "Show Relevant now",
            "Show active projects",
            "Show project widgets",
            "Included projects",
            "Metrics",
            "Relevant now groups",
            "Hide empty groups",
            "Active projects"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::dashboard"
        }
      }
    },
    {
      "text": "The Product shows the chosen metrics, the Relevant now groups and the active projects for the workspace's todos and shared projects",
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
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": [
            "Name",
            "Color"
          ]
        },
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::dashboard"
        }
      }
    }
  ]
}
---

# Open the dashboard

## Trigger

A person starts their day.

## Outcome

The person sees what is overdue, due today and most active, and can drill into any tile.
