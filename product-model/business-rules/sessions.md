---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "sign-in"
    },
    {
      "type": "capability",
      "id": "sign-out"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/auth.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "docs/architecture.md"
    }
  ]
}
---

# A sign-in lasts 30 days and is extended while used

A person stays signed in on a device for 30 days, renewed while they use it, until they sign out there or their password changes.
