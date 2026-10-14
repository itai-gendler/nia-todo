---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "user",
      "effect": "creates"
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

# Only the administrator creates accounts

There is no self-registration: the first account comes from first-run setup and every other from the administrator.
