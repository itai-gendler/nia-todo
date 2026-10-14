---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User opens a Todo and changes its title, description, priority, project, section, repeat or pin",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Title",
            "Description",
            "Priority",
            "Project",
            "Section",
            "Repeat",
            "Pinned"
          ]
        },
        {
          "entity": "project",
          "effect": "reads",
          "facts": []
        },
        {
          "entity": "section",
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
      "text": "The Product saves the todo for everyone who can see it",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Title",
            "Description",
            "Priority",
            "Project",
            "Section",
            "Repeat",
            "Pinned"
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

# Change a todo

## Trigger

A todo turns out to be more urgent.

## Outcome

Everyone in the project sees the change at once; offline changes follow when the device is back online.

## Edge cases

- A section must belong to the chosen project.
