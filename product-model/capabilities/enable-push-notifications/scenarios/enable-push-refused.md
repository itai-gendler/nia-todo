---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enables notifications in a browser that blocks or does not support them",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::notification-settings"
        }
      }
    },
    {
      "text": "The Product explains that permission is blocked or push is unsupported and registers nothing",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::notification-settings"
        }
      }
    }
  ]
}
---

# Enable push where the browser does not allow it

## Trigger

A person denied the notification permission earlier.

## Outcome

No subscription is created; the person can allow notifications in the browser settings.
