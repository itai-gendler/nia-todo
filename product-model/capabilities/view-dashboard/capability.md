---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "view",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/app-rendering.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/dashboard-preferences.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/dashboard-drilldown.js"
    }
  ]
}
---

# View dashboard

A person opens the dashboard of the current workspace: metric tiles, the Relevant now groups (Overdue, Due today, Next 7 days, High priority) and the active projects, as their dashboard preferences shape it.
