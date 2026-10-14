---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "attachment",
      "facts": [
        "Size"
      ]
    },
    {
      "type": "entity",
      "id": "user",
      "facts": [
        "Attachment quota"
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/attachments.py"
    }
  ]
}
---

# Attachments count against the uploader's storage

Storage is counted per uploader, whoever owns the project; the person's own quota applies, or the server default when none is set.
