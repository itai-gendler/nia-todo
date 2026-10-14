---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "connect-to-server"
    },
    {
      "type": "entity",
      "id": "server-connection"
    },
    {
      "type": "entity",
      "id": "instance-settings",
      "facts": [
        "Minimum app version"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/core/config.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/app-downloads.js"
    }
  ]
}
---

# Apps connect only to a verified nia-todo server over HTTPS

An app saves a server only after it answers as nia-todo; the address must use HTTPS unless the server is on the same machine (localhost), and must not carry credentials. An app older than the server's minimum app version is asked to update.
