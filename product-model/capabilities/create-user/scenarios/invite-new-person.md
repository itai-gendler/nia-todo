---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator enters a username, display name, email address and language, and whether BrainDump is allowed",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "creates",
          "facts": [
            "Username",
            "Display name",
            "Email",
            "Language",
            "BrainDump access"
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
      "text": "The Product creates the User with a Personal Workspace holding an Inbox and the projects Personal, Work and Shopping, and an invitation Password link",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "user",
          "effect": "creates",
          "facts": [
            "Username",
            "Display name",
            "Email",
            "Language",
            "BrainDump access",
            "First user"
          ]
        },
        {
          "entity": "workspace",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
            "Default",
            "Order"
          ],
          "with": "user"
        },
        {
          "entity": "project",
          "as": "inbox",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Icon",
            "Workspace",
            "Inbox",
            "Order"
          ],
          "with": "workspace"
        },
        {
          "entity": "project",
          "as": "starter-project",
          "effect": "creates",
          "facts": [
            "Name",
            "Color",
            "Order",
            "Workspace",
            "Inbox"
          ],
          "with": "workspace"
        },
        {
          "entity": "password-link",
          "effect": "creates",
          "to": "Active",
          "facts": [
            "Purpose",
            "Expires at",
            "Requested by"
          ],
          "with": "user"
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    },
    {
      "text": "The Product emails the invitation in the person's language and says so",
      "kind": "product",
      "actor": "administrator",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::administration::users"
        }
      }
    }
  ]
}
---

# Create an account and invite the person

## Trigger

A family member wants their own todo list on the server.

## Outcome

The person can set their password from the email and sign in.

## Decision points

### Email delivery

Can the server send email?

- Email delivery is configured and the email is sent → the invitation goes to the person by email
- No email delivery, or sending fails → the administrator gets the link to pass on themselves
