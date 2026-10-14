---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens the invitation Password link",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "password-link",
          "effect": "reads",
          "facts": [
            "Purpose",
            "Expires at"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username",
            "Display name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      }
    },
    {
      "text": "The User chooses a password that meets the password rules",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      }
    },
    {
      "text": "The Product sets the password, confirms the email address and marks the Password link used",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password",
            "Email verified"
          ]
        },
        {
          "entity": "password-link",
          "effect": "changes",
          "from": "Active",
          "to": "Used",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      }
    },
    {
      "text": "The Product tells the person they can now sign in and offers the way into the app",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      }
    }
  ]
}
---

# Choose a password from an invitation link

## Trigger

A new person receives the invitation email or the link from the administrator.

## Outcome

The account has a password and a confirmed email; the person can sign in.
