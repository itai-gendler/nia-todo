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
      "target": "api/migrations/043_add_location_reminders.sql"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src-tauri/gen/android/app/src/main/java/de/tobiaskneidl/nia_todo/LocationReminderReceiver.kt"
    }
  ]
}
---

# Location reminder

A reminder that notifies one person when they arrive at or leave an address. It is kept on the server and triggered by the Android app.

## Information kept

- **Trigger** — When arriving or When leaving
- **Address** — the address it watches, from a saved place or typed in
- **Enabled** — whether it is active
