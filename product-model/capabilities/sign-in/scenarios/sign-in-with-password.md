---
{
  "kind": "primary",
  "routes": {
    "web": "Web",
    "desktop": "Desktop app",
    "android": "Android app"
  },
  "steps": [
    {
      "text": "The User enters their username or verified email address and their password",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        },
        "desktop": {
          "place": "desktop-app::sign-in::sign-in"
        },
        "android": {
          "place": "android-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The username or verified email names an account and the password matches it",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username",
            "Email",
            "Email verified",
            "Password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        },
        "desktop": {
          "place": "desktop-app::sign-in::sign-in"
        },
        "android": {
          "place": "android-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The Product signs the person in and opens the app",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        },
        "desktop": {
          "place": "desktop-app::sign-in::sign-in"
        },
        "android": {
          "place": "android-app::sign-in::sign-in"
        }
      }
    }
  ]
}
---

# Sign in with username or email and password

## Trigger

A person opens the app on the web, the desktop app or the Android app and is not signed in.

## Outcome

The person is signed in on this device for 30 days, renewed while they keep using it.

## Edge cases

- An email address that is not verified does not sign anyone in; the username still does.
- When the account must confirm a second factor and this device is not remembered, the person confirms it before the app opens.
