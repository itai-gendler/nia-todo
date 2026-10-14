---
{
  "singleton": true,
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/instance_config.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/email_config.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/attachments.py"
    }
  ]
}
---

# Instance settings

The server-wide settings the administrator keeps, one set per server.

## Information kept

- **Setup complete** — whether first-run setup has finished
- **Admin password** — the password that opens the administration area
- **Public address** — the HTTPS address people and apps reach the server at, used in emailed links
- **Update analytics** — whether the server shares anonymous update statistics
- **Email delivery** — the outgoing mail server, its security mode and sender; Configured once complete
- **Password link validity** — how many hours a password or email confirmation link stays valid, 1 to 168, 24 by default
- **Attachments enabled** — whether people may upload attachments; On by default
- **Allowed attachment types** — the file extensions and types people may upload; images and PDF by default
- **Default attachment quota** — the storage each person may use for attachments unless their account sets its own; 5 GB by default
- **Minimum app version** — the oldest desktop or Android app version the server still serves
