---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator deletes an account and confirms",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Username",
            "First user"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The Product deletes the User with their workspaces, projects, todos, places and API keys",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "removes"
        },
        {
          "entity": "workspace",
          "effect": "removes",
          "with": "user"
        },
        {
          "entity": "project",
          "effect": "removes",
          "with": "user"
        },
        {
          "entity": "todo",
          "effect": "removes",
          "from": "Open",
          "with": "user"
        },
        {
          "entity": "place",
          "effect": "removes",
          "with": "user"
        },
        {
          "entity": "api-key",
          "effect": "removes",
          "from": "Active",
          "with": "user"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    }
  ]
}
---

# Delete an account

## Trigger

A person leaves the household.

## Outcome

The account and everything it owned are gone.

## Edge cases

- Todos the person created in other people's shared projects are deleted too, as are their comments and attachments.
