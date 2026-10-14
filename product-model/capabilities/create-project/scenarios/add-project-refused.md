---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User creates a project under a parent that is in another workspace, or that they do not own",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "effect": "creates",
          "facts": [
            "Name",
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
      "text": "The Product refuses",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::app::project-editor"
        }
      }
    }
  ]
}
---

# Create a subproject under a parent in another workspace

## Trigger

A person picks a parent from the wrong workspace.

## Outcome

No project is created.
