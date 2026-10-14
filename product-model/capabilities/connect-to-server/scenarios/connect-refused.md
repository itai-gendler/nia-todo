---
{
  "kind": "validation",
  "routes": {
    "desktop": "Desktop app"
  },
  "steps": [
    {
      "text": "The User enters an address that is unreachable, not HTTPS, contains credentials or does not identify itself as the app's server",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::server-setup"
        }
      }
    },
    {
      "text": "The Product refuses and says which check failed",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "desktop": {
          "place": "desktop-app::sign-in::server-setup"
        }
      }
    }
  ]
}
---

# Connect to an address that is not a nia-todo server

## Trigger

A person mistypes the address.

## Outcome

Nothing is saved; the app stays on server setup.
