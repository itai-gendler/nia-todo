---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User names a new API key",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "creates",
          "to": "Active",
          "facts": [
            "Name"
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
      "text": "The Product creates the API key and shows the full key once",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "api-key",
          "effect": "creates",
          "to": "Active",
          "facts": [
            "Name",
            "Prefix",
            "Key",
            "Created at"
          ]
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

# Create an API key

## Trigger

A person connects a script to their todos.

## Outcome

The key works for the API on the person's behalf until revoked; afterwards only its prefix is shown.
