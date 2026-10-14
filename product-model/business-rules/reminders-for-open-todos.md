---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "send-reminder"
    },
    {
      "type": "entity",
      "id": "reminder",
      "facts": [
        "Remind at"
      ]
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

# Only reminders of open todos are sent

A reminder whose todo is done is not sent, and each reminder is sent once.
