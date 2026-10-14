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
      "target": "web/static/js/features/dashboard-preferences-dialog.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/dashboard-preferences-sync.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/me.py"
    }
  ]
}
---

# Customize dashboard

A person shapes the dashboard of each workspace: layout, content, included projects, the four metrics, the Relevant now groups and the active projects list. The choices stay on the device unless the person syncs them through their account.
