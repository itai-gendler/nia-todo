---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User changes the layout, content, included projects, metrics and groups for a Workspace",
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
          "effect": "changes",
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
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::dashboard"
        }
      }
    },
    {
      "text": "The Product saves the Dashboard preferences for that workspace",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "dashboard-preferences",
          "effect": "changes",
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

# Customize a workspace's dashboard

## Trigger

A person wants only high-priority work on their Work dashboard.

## Outcome

That workspace's dashboard shows what the person chose.

## Edge cases

- Exactly four different metrics must be chosen.
- Included projects must belong to the workspace.
