---
{
  "type": "mobile-app",
  "actors": [
    "user"
  ],
  "languages": [
    "de",
    "en",
    "cs",
    "fr",
    "it",
    "nl",
    "pl",
    "pt-BR",
    "ru",
    "sv",
    "es",
    "zh-CN"
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "src-tauri/gen/android/app/src/main/java/de/tobiaskneidl/nia_todo/MainActivity.kt"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src-tauri/gen/android/app/src/main/java/de/tobiaskneidl/nia_todo/ReminderReceiver.kt"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/native-bridge.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "docs/architecture.md"
    }
  ]
}
---

# Android app

The Android app. It bundles the app locally, connects to one nia-todo server, schedules reminders on the phone and triggers location reminders.
