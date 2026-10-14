---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator signs out of administration",
      "kind": "actor",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::administration"
        }
      }
    },
    {
      "text": "The Product ends every administration session and returns to the admin sign-in",
      "kind": "product",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::administration"
        }
      }
    }
  ]
}
---

# Sign out of administration

## Trigger

The administrator is done.

## Outcome

Nobody is signed in to administration until the admin password is entered again.
