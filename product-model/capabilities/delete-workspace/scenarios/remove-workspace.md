---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User deletes a Workspace and confirms",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "workspace",
          "effect": "reads",
          "facts": [
            "Name"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::workspace-editor"
        }
      }
    },
    {
      "text": "The Product moves the workspace's projects to the default workspace, its Inbox todos to the default Inbox, and deletes the workspace with its Inbox",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "project",
          "as": "moved-project",
          "effect": "changes",
          "facts": [
            "Workspace"
          ]
        },
        {
          "entity": "todo",
          "effect": "changes",
          "facts": [
            "Project",
            "Section"
          ]
        },
        {
          "entity": "workspace",
          "effect": "removes"
        },
        {
          "entity": "project",
          "as": "inbox",
          "effect": "removes",
          "with": "workspace"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::workspace-editor"
        }
      }
    }
  ]
}
---

# Delete a workspace

## Trigger

A person finished a side project and wants one workspace less.

## Outcome

Nothing in the workspace is lost; its projects and Inbox todos are in the default workspace.
