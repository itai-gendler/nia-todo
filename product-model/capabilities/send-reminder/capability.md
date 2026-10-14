---
{
  "availability": [
    {
      "place": "web-app::app"
    },
    {
      "place": "desktop-app::app"
    },
    {
      "place": "android-app::app"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/push.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/main.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/native-bridge.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src-tauri/gen/android/app/src/main/java/de/tobiaskneidl/nia_todo/ReminderReceiver.kt"
    }
  ]
}
---

# Send reminder

When a reminder's time comes and its todo is still open, the Product notifies the person: by push to their browsers, on their open desktop apps, and through the Android app's own alarm.
