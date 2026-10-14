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
      "id": "comment"
    },
    {
      "type": "entity",
      "id": "attachment"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/websocket.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/websocket-client.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "docs/architecture.md"
    }
  ]
}
---

# Changes in a project reach everyone in it at once

Changes to a project's todos, sections, subtasks, comments and attachments appear immediately for the owner and every member who is online; a person's own changes reach all their devices.
