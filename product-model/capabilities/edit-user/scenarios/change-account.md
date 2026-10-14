---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator changes the username, display name, BrainDump access or storage quota of an account",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Username",
            "Display name",
            "BrainDump access",
            "Attachment quota"
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
      "text": "The Product saves the changes",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Username",
            "Display name",
            "BrainDump access",
            "Attachment quota"
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

# Change an account

## Trigger

A person needs more storage for attachments.

## Outcome

The account works with its new settings; an empty quota falls back to the server default.
