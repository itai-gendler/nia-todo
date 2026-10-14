---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User switches to Multiple todos and enters one todo per line, with shared defaults for all of them",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "facts": [
            "Title",
            "Priority",
            "Project",
            "Section",
            "Deadline"
          ],
          "to": "Open"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "The Product creates one Todo per line, applying Quick Add details per line over the defaults",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "creates",
          "to": "Open",
          "facts": [
            "Title",
            "Description",
            "Priority",
            "Pinned",
            "Project",
            "Section",
            "Deadline",
            "Repeat"
          ]
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

# Create several todos at once

## Trigger

A person pastes a packing list.

## Outcome

Each line is its own todo; up to 50 lines at once.
