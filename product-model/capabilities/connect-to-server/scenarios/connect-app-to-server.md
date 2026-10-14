---
{
  "kind": "primary",
  "routes": {
    "desktop": "Desktop app",
    "android": "Android app"
  },
  "steps": [
    {
      "text": "The User enters the server's address",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::server-setup"
        },
        "android": {
          "place": "android-app::sign-in::server-setup"
        }
      }
    },
    {
      "text": "The Product checks the address uses HTTPS and asks the server to identify itself",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::server-setup"
        },
        "android": {
          "place": "android-app::sign-in::server-setup"
        }
      }
    },
    {
      "text": "The Product saves the Server connection and shows sign-in",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "server-connection",
          "effect": "creates",
          "facts": [
            "Server address",
            "Verified instance"
          ]
        }
      ],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::server-setup"
        },
        "android": {
          "place": "android-app::sign-in::server-setup"
        }
      }
    }
  ]
}
---

# Connect the app to a nia-todo server

## Trigger

A person installs the desktop or Android app.

## Outcome

The app talks to that server from now on, even when it starts offline.

## Edge cases

- A plain-HTTP address is accepted only for a server on the same machine (localhost).
- When the server requires a newer app than the one installed, the app asks the person to update it.
