---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User revokes one of their API keys and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "reads",
          "facts": [
            "Name",
            "Prefix",
            "Created at",
            "Last used"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::api-key-settings"
        }
      }
    },
    {
      "text": "The Product stops accepting the API key",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "changes",
          "from": "Active",
          "to": "Revoked",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::api-key-settings"
        }
      }
    }
  ]
}
---

# Revoke an API key

## Trigger

An automation is retired or its key leaked.

## Outcome

Requests with that key are refused; the key stays listed as revoked.
