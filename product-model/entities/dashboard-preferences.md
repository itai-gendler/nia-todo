---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/me.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/dashboard-preferences.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/054_add_dashboard_preferences_sync.sql"
    }
  ]
}
---

# Dashboard preferences

How one person's dashboard looks for one of their workspaces. They stay on the device unless the person syncs them through their account.

## Information kept

- **Compact display** — whether the dashboard uses the compact layout
- **Group by status** — whether todos are grouped by status
- **Show Relevant now** — whether the Relevant now groups are shown
- **Show active projects** — whether the active projects list is shown
- **Show project widgets** — whether project widgets are shown
- **Included projects** — all projects, only selected ones, or all but selected ones
- **Metrics** — the four metric tiles and their order
- **Relevant now groups** — which of Overdue, Due today, Next 7 days and High priority appear
- **Hide empty groups** — whether empty groups are hidden
- **Active projects** — how many active projects are listed (2, 4 or 6) and how they are sorted
