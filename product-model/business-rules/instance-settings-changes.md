---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "instance-settings",
      "effect": "changes"
    }
  ],
  "permits": [
    {
      "actors": [
        "administrator"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/setup.py"
    }
  ]
}
---

# Only the administrator changes the instance settings

Server-wide settings are set during first-run setup and in the administration area.
