---
{
  "type": "desktop-app",
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
      "target": "src-tauri/src/lib.rs"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "src-tauri/tauri.conf.json"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/native-bridge.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/desktop-integration.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "docs/architecture.md"
    }
  ]
}
---

# Desktop app

The Windows and Debian desktop app. It bundles the app locally, connects to one nia-todo server, and shows reminders as desktop notifications.
