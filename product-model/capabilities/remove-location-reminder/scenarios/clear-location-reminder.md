---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User turns off the location reminder of a Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "location-reminder",
          "effect": "reads",
          "facts": [
            "Trigger",
            "Address"
          ]
        },
        {
          "entity": "todo",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The Product removes the person's Location reminder",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "location-reminder",
          "effect": "removes"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    }
  ]
}
---

# Remove a location reminder

## Trigger

The errand is done elsewhere.

## Outcome

The person is no longer reminded at that place.
