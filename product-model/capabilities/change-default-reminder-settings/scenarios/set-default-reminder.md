---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses how long before a deadline to be reminded, or none",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Default reminder"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::default-reminder-settings"
        }
      }
    },
    {
      "text": "The Product saves it for deadlines set from now on",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "user",
          "effect": "changes",
          "facts": [
            "Default reminder"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::default-reminder-settings"
        }
      }
    }
  ]
}
---

# Set the automatic reminder for deadlines

## Trigger

A person wants a nudge an hour before anything is due.

## Outcome

Todos given a deadline from now on get an automatic Reminder that much earlier, unless the person chooses a reminder time themselves.

## Edge cases

- The offset can be up to one year.
