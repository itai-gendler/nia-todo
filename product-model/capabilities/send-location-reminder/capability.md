---
{
  "availability": [
    {
      "place": "android-app::app"
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
      "target": "web/static/js/features/native-bridge.js"
    }
  ]
}
---

# Send location reminder

The Android app notifies a person when they arrive at or leave the address of one of their location reminders, and keeps watching after the phone restarts.
