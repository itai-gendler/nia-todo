---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator submits setup with a missing or wrong token, or after setup finished",
      "kind": "actor",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::first-run-setup"
        }
      }
    },
    {
      "text": "The token is not the current one-time token, or setup is already complete",
      "kind": "condition",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Setup complete"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::first-run-setup"
        }
      }
    },
    {
      "text": "The Product refuses and changes nothing",
      "kind": "product",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::first-run-setup"
        }
      }
    }
  ]
}
---

# Run setup without a valid token or after it finished

## Trigger

Someone reaches /setup on a server that is already running, or without access to its log.

## Outcome

No admin password or account is created.
