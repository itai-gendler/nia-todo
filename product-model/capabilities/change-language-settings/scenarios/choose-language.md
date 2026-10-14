---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses Automatic or one of the twelve languages",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Language"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::language-settings"
        }
      }
    },
    {
      "text": "The Product saves it and shows the app in that language; the server's emails to the person use it too",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Language"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::language-settings"
        }
      }
    }
  ]
}
---

# Choose a language

## Trigger

A person prefers Dutch over their browser language.

## Outcome

The app and the emails the person receives use the chosen language.
