---
{
  "availability": [
    {
      "place": "web-app::administration"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/admin.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/instance_config.py"
    }
  ]
}
---

# Change instance settings

The administrator sets the server's public address, used for emailed links and app sign-in, and whether anonymous update statistics are shared.
