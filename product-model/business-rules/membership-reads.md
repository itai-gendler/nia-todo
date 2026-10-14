---
{
  "appliesTo": [
    {
      "type": "entity",
      "id": "project-membership",
      "effect": "reads"
    }
  ],
  "permits": [
    {
      "related": [
        {
          "verb": "holds",
          "entity": "user"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "project"
        },
        {
          "verb": "owns",
          "entity": "user"
        }
      ]
    },
    {
      "related": [
        {
          "verb": "has",
          "entity": "project"
        },
        {
          "verb": "has",
          "entity": "project-membership"
        },
        {
          "verb": "holds",
          "entity": "user"
        }
      ],
      "when": [
        {
          "state": "Accepted"
        }
      ]
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/sharing.py"
    }
  ]
}
---

# Pending invitations are seen only by the invitee and the owner

Members of a shared project see each other once accepted; a pending invitation stays between the owner and the invitee.
