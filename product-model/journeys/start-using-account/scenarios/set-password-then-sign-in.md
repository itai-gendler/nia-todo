---
{
  "kind": "primary",
  "result": "achieved",
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
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      },
      "capability": "set-password"
    },
    {
      "text": "The User chooses a password",
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
      },
      "capability": "set-password"
    },
    {
      "text": "The Product sets the password, confirms the email, marks the Password link used and offers the way into the app",
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
      },
      "capability": "set-password"
    },
    {
      "text": "The User signs in with their username and new password",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
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
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      },
      "capability": "sign-in"
    }
  ]
}
---

# Choose a password from the invitation and sign in

## Trigger

An invitation email arrives.

## Outcome

The person is in the app with their Personal workspace and starter projects.
