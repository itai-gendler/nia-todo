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
    }
  ]
}
---

# Edit place

A person changes a saved place's label, address or icon. A new address carries over to the location reminders that use the place.
