---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "todo"
    },
    {
      "type": "entity",
      "id": "section"
    },
    {
      "type": "entity",
      "id": "subtask"
    },
    {
      "type": "entity",
      "id": "comment"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/sync/queue.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/sync.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "README.md"
    }
  ]
}
---

# Changes made offline are kept and sent later

Creating, changing, moving and deleting todos and sections works offline: changes are kept on the device and sent when the server is reachable. Subtasks, comments, attachments and workspace changes need a connection.
