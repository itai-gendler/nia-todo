---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator asks for a password link for an account",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username",
            "Email",
            "Email verified"
          ]
        },
        {
          "entity": "password-link",
          "as": "new-link",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The Product replaces any earlier active reset Password link with a new one",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "password-link",
          "as": "earlier-link",
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
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The Product emails the Password link to a verified address, or shows it to the administrator to pass on",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "password-link",
          "as": "new-link",
          "effect": "reads",
          "facts": []
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

# Send a password link

## Trigger

A person is locked out and the server cannot email resets to them.

## Outcome

The person sets a new password through the link within its validity.
