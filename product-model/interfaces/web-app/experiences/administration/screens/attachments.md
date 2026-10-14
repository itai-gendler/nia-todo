---
{
  "entities": [
    {
      "entity": "instance-settings",
      "collects": [
        "Attachments enabled",
        "Allowed attachment types",
        "Default attachment quota"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/admin.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/pages/admin.js"
    }
  ]
}
---

# Attachments

Whether attachments are allowed, which types, and the default storage per person.
