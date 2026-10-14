---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User asks for a password reset with their username or email",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The server can send email and an account with that username or verified email exists",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Email delivery"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username",
            "Email",
            "Email verified"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The Product creates a reset Password link and emails it to the verified address",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "password-link",
          "effect": "creates",
          "to": "Active",
          "facts": [
            "Purpose",
            "Expires at",
            "Requested by"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The Product confirms that an email was sent if an account matched",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The User opens the Password link and chooses a new password",
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
      "text": "The Product sets the password, marks the Password link used and signs the account out of every device",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Password"
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
    }
  ]
}
---

# Reset a forgotten password through the emailed link

## Trigger

A person cannot remember their password.

## Outcome

The person has a new password and signs in again with it.

## Edge cases

- The answer is the same whether or not an account matched, so it never reveals who has an account.
- A new reset link replaces any earlier active reset link for the account.
- If the email cannot be sent, the new link is withdrawn and the answer stays the same.
