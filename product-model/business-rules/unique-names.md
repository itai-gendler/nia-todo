---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "workspace",
      "facts": [
        "Name"
      ]
    },
    {
      "type": "entity",
      "id": "place",
      "facts": [
        "Name"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/016_add_workspaces.sql"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/043_add_location_reminders.sql"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "CHANGELOG.md"
    }
  ]
}
---

# Workspace and place names are unique per person

A person cannot have two workspaces, or two places, with the same name; place labels are compared ignoring case. Projects are told apart by identity, so their names may repeat.
