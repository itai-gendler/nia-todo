---
{
  "kind": "alternative",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User picks another of their workspaces for a Project they own",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "as": "project",
          "effect": "changes",
          "facts": [
            "Workspace",
            "Parent project"
          ]
        },
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": []
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    },
    {
      "text": "The Product moves the project and all its subprojects to that workspace",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "as": "project",
          "effect": "changes",
          "facts": [
            "Workspace"
          ]
        },
        {
          "entity": "project",
          "as": "subproject",
          "effect": "changes",
          "facts": [
            "Workspace"
          ]
        },
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": []
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

# Move a project to another workspace

## Trigger

A side project becomes work.

## Outcome

The project and its subprojects belong to the other workspace; members keep their own display workspace.
