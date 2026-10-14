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
      "target": "api/migrations/043_add_location_reminders.sql"
    }
  ]
}
---

# Delete place

A person deletes a saved place. Location reminders that used it keep watching its last address.
