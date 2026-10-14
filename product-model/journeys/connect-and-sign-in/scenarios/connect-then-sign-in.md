---
{
  "kind": "primary",
  "result": "achieved",
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
      },
      "capability": "connect-to-server"
    },
    {
      "text": "The Product verifies the server, saves the Server connection and shows sign-in",
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
      },
      "capability": "connect-to-server"
    },
    {
      "text": "The User enters their username or verified email and password",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::sign-in"
        },
        "android": {
          "place": "android-app::sign-in::sign-in"
        }
      },
      "capability": "sign-in"
    },
    {
      "text": "The Product signs them in and opens the app",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::sign-in"
        },
        "android": {
          "place": "android-app::sign-in::sign-in"
        }
      },
      "capability": "sign-in"
    }
  ]
}
---

# Connect a new app and sign in

## Trigger

A person installs the app on a new laptop or phone.

## Outcome

The person works in the app, which keeps the server for later starts.
