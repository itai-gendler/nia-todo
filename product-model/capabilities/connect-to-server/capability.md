---
{
  "availability": [
    {
      "place": "desktop-app::sign-in"
    },
    {
      "place": "android-app::sign-in"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/core/config.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/main.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/instance.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/instance_config.py"
    }
  ]
}
---

# Connect to server

Before anyone signs in, the desktop or Android app is connected to a nia-todo server. The app checks the address and asks the server to identify itself before saving it.
