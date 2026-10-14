---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "send-location-reminder"
    },
    {
      "type": "entity",
      "id": "location-reminder"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src-tauri/gen/android/app/src/main/java/de/tobiaskneidl/nia_todo/LocationReminderReceiver.kt"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/i18n/en.json"
    }
  ]
}
---

# Location reminders fire only in the Android app

Location reminders can be set everywhere, but only the Android app watches places and notifies.
