---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters the one-time setup token from the server log",
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
      "text": "The Administrator chooses the admin password",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Admin password"
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
      "text": "The Administrator enters the first account's username, display name, email address and password",
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
      "text": "The Product creates the first User with a verified email and a Personal Workspace, completes setup and deletes the setup token",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "creates",
          "facts": [
            "Username",
            "Display name",
            "Email",
            "Email verified",
            "Password",
            "First user"
          ]
        },
        {
          "entity": "workspace",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
            "Default",
            "Order"
          ],
          "with": "user"
        },
        {
          "entity": "instance-settings",
          "effect": "changes",
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
      "text": "The Product sends the person on to the app",
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

# Set up a new server

## Trigger

Someone has just installed nia-todo and opens /setup.

## Outcome

The server has its admin password and its first account; setup cannot run again.
