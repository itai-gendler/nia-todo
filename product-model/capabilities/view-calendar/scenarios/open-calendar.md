---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens the calendar and picks month, week or day",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::calendar"
        }
      }
    },
    {
      "text": "The Product puts each todo with a deadline on its day, timed ones in the timeline and the rest under All day",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title",
            "Priority",
            "Deadline"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::calendar"
        }
      }
    }
  ]
}
---

# Look at the calendar

## Trigger

A person plans their week.

## Outcome

The person sees when their todos are due.

## Edge cases

- Done todos can be hidden.
