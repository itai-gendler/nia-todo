---
{
  "domain": "workspaces",
  "relations": [
    {
      "entity": "project",
      "verb": "contains",
      "cardinality": "one-to-many"
    },
    {
      "entity": "dashboard-preferences",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/workspaces.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/016_add_workspaces.sql"
    }
  ]
}
---

# Workspace

A person's own context for grouping projects, such as Private or Work. Each account starts with a Personal workspace, its default; every workspace has its own Inbox. Workspaces are never shared.

## Information kept

- **Name** — what the workspace is called, unique among the person's workspaces
- **Color** — the color it is shown with
- **Icon** — an optional icon
- **Default** — whether this is the Personal workspace every account starts with
- **Order** — where it sits among the person's workspaces
