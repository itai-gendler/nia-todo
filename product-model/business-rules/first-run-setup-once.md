---
{
  "appliesTo": [
    {
      "type": "capability",
      "id": "complete-first-run-setup"
    },
    {
      "type": "entity",
      "id": "instance-settings",
      "facts": [
        "Setup complete"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/setup_token.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/setup.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "README.md"
    }
  ]
}
---

# First-run setup runs once and needs the token from the server log

Setup is protected by a one-time token the server prints to its log; it is deleted when the first account is created, and setup cannot run again.
