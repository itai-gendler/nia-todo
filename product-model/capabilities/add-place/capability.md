---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "places",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/places.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/user-settings.js"
    }
  ]
}
---

# Add place

A person saves a labelled address, such as Home, for location reminders.
