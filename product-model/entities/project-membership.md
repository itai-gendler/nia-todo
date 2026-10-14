---
{
  "domain": "projects",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/sharing.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/services/sharing.py"
    }
  ]
}
---

# Project membership

One person's place in a project someone else owns: an invitation first, then access once accepted. Leaving or being removed keeps the membership so it can be restored.

## Information kept

- **Display workspace** — which of the member's own workspaces shows the shared project; their default workspace unless they choose another
- **Invited by** — the owner who sent the invitation
- **Invited with** — whether the owner named the person by username or by email

## States

### Pending

Invited and waiting for the person to accept or decline; only the invitee and the owner see it.

### Accepted

The person works in the project with its owner and other members.

### Declined

The person declined the invitation.

### Left

The person left the project.

### Removed

The owner removed the person or withdrew the invitation.
