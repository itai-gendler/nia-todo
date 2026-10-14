---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User chooses or drops one or more files on a Todo",
      "kind": "actor",
      "actor": "user",
      "entities": [
        {
          "entity": "todo",
          "effect": "reads",
          "facts": [
            "Title"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::app::todo-editor"
        }
      }
    },
    {
      "text": "Attachments are enabled, the type is allowed, the file is at most 25 MB and fits in the person's storage",
      "kind": "condition",
      "actor": "user",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "reads",
          "facts": [
            "Attachments enabled",
            "Allowed attachment types",
            "Default attachment quota"
          ]
        },
        {
          "entity": "user",
          "effect": "reads",
          "facts": [
            "Attachment quota"
          ]
        },
        {
          "entity": "attachment",
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
      "text": "The Product stores each Attachment with its uploader and shows the remaining storage",
      "kind": "product",
      "actor": "user",
      "entities": [
        {
          "entity": "attachment",
          "effect": "creates",
          "facts": [
            "File name",
            "File type",
            "Size",
            "Uploaded at",
            "File content"
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

# Attach a file to a todo

## Trigger

A person adds the receipt photo to a todo.

## Outcome

Everyone with access to the todo can preview or download the file.
