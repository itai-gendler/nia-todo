---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User turns on Sync through my account",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Dashboard sync"
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
      "text": "The Product keeps the Dashboard preferences of every workspace in the account and applies them on every signed-in device",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Dashboard sync"
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

# Sync dashboard preferences through the account

## Trigger

A person wants the same dashboard on phone and laptop.

## Outcome

Every signed-in app and browser of the person shows the same dashboards; turning sync off removes them from the account.
