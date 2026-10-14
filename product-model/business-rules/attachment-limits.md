---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "upload-attachment"
    },
    {
      "type": "entity",
      "id": "attachment",
      "facts": [
        "File type",
        "Size"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/attachments.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    }
  ]
}
---

# Attachments are limited in type, size, number and storage

Each file is at most 25 MB and of an allowed type, checked against its content for images, PDF and ZIP; a todo holds at most 20 attachments; and a person's uploads may not exceed their storage quota.
