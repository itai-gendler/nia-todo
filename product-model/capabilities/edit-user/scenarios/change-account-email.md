---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters a new email address for an account",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Email"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The server can send email",
      "kind": "condition",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Email delivery"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The Product records the address as pending and emails the person a confirmation link",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Pending email"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    }
  ]
}
---

# Change an account's email address

## Trigger

A person's address changed.

## Outcome

The person confirms the new address; on a server without email it is saved as verified at once.

## Edge cases

- A username or email another account uses is refused.
