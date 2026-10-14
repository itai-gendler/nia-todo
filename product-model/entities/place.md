---
{
  "domain": "places",
  "relations": [
    {
      "entity": "location-reminder",
      "verb": "anchors",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/places.py"
    }
  ]
}
---

# Place

A labelled address a person saves, such as Home or Work, to use in location reminders and BrainDump.

## Information kept

- **Name** — the label, up to 120 characters and unique among the person's places
- **Address** — the street address
- **Icon** — an icon; a pin by default
