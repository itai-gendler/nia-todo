---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User deletes a Project they own and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "as": "deleted-project",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "The Product moves every todo of the project and its subprojects to its creator's Inbox, then deletes the subprojects, the sections and the project",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Project",
            "Section"
          ]
        },
        {
          "entity": "project",
          "as": "deleted-project",
          "effect": "removes"
        },
        {
          "entity": "project",
          "as": "subproject",
          "effect": "removes",
          "with": "deleted-project"
        },
        {
          "entity": "section",
          "effect": "removes",
          "with": "deleted-project"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    }
  ]
}
---

# Delete a project

## Trigger

A project is finished and its open todos should not be lost.

## Outcome

The project is gone for the owner and every member; nobody's todos are lost.
