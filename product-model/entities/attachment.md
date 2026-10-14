---
{
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/attachments.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/050_add_todo_attachments.sql"
    }
  ]
}
---

# Attachment

A file or photo uploaded to a todo, counted against the storage of the person who uploaded it.

## Information kept

- **File name** — the name the file was uploaded with
- **File type** — the kind of file, detected from its content where the type requires it
- **Size** — the file size, at most 25 MB
- **Uploaded at** — when it was uploaded
- **File content** — the stored file itself
