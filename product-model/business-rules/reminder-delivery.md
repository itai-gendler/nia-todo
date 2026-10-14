---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "reminder",
      "effect": "changes",
      "to": "Sent"
    }
  ],
  "permits": [
    {
      "unattended": true
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/push.py"
    }
  ]
}
---

# Reminders are sent by the Product on its own

Nobody marks a reminder sent by hand; the Product sends it when it is due.
