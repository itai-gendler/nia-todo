---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/reminders.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/push.py"
    }
  ]
}
---

# Reminder

A time at which one person is notified about a todo. Each person keeps their own reminder on a shared todo.

## Information kept

- **Remind at** — when the notification is due
- **Source** — Automatic when it follows the deadline by the person's default reminder, Chosen when the person set the time

## States

### Scheduled

Waiting for its time.

### Sent

The notification went out.
