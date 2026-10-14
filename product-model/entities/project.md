---
{
  "domain": "projects",
  "relations": [
    {
      "entity": "section",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "project-membership",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "todo",
      "verb": "contains",
      "cardinality": "one-to-many"
    },
    {
      "entity": "project",
      "verb": "parents",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/projects.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/011_add_project_sharing.sql"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/012_add_inbox_project_flag.sql"
    }
  ]
}
---

# Project

A list of todos a person owns, inside one of their workspaces, optionally under a parent project as a subproject and divided into sections. Each workspace has one Inbox project. The owner can share a project with other people on the server.

## Information kept

- **Name** — what the project is called; several projects may share a name
- **Color** — the color it is shown with
- **Icon** — an optional icon
- **Parent project** — the owner's project this one sits under, in the same workspace, or none
- **Workspace** — the owner's workspace the project belongs to
- **Inbox** — whether this is the workspace's Inbox, where todos without a project land
- **Order** — where it sits among its siblings
