---
{
  "kind": "edge",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a Password link that has expired",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "password-link",
          "as": "password-link",
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
      }
    },
    {
      "text": "The server can send email to the account's address",
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
            "Email"
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
      "text": "The User asks for a new link",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::set-password"
        }
      }
    },
    {
      "text": "The Product replaces the expired Password link with a new one of the same purpose and emails it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "password-link",
          "as": "expired-link",
          "effect": "changes",
          "from": "Active",
          "to": "Replaced",
          "facts": []
        },
        {
          "entity": "password-link",
          "as": "new-link",
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
          "place": "web-app::sign-in::set-password"
        }
      }
    }
  ]
}
---

# Ask for a new link after the old one expired

## Trigger

A person opens their invitation days after it was sent.

## Outcome

A fresh link is on its way by email.

## Edge cases

- When the server cannot email the account, the page asks the person to contact an admin instead.
