---
{
  "relations": [
    {
      "entity": "subtask",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "comment",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "attachment",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "reminder",
      "verb": "has",
      "cardinality": "one-to-many"
    },
    {
      "entity": "location-reminder",
      "verb": "has",
      "cardinality": "one-to-many"
    }
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/todos.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/001_initial_schema.sql"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/migrations/041_add_todo_recurrence_columns.sql"
    }
  ]
}
---

# Todo

A task in a project: what needs doing, how urgent it is, when it is due, and its checklist, comments, attachments and reminders. A todo may repeat; completing a repeating todo creates its next occurrence.

## Information kept

- **Title** — what needs to be done, up to 500 characters
- **Description** — optional details in Markdown, up to 50,000 characters
- **Priority** — Very high, High, Medium or Low; Medium by default
- **Pinned** — whether the todo is pinned to the top of its lists
- **Project** — the project it belongs to; the Inbox when none is chosen
- **Section** — the section of its project it sits in, or Unsorted
- **Deadline** — the date, and optionally time, it is due
- **Repeat** — Daily, Weekly, Monthly or Yearly every 1 to 999 periods, kept in the person's time zone; none by default
- **Completed at** — when it was last marked done
- **Series** — the first todo of the repeating series this occurrence belongs to

## States

### Open

Waiting to be started.

### In progress

Being worked on.

### Done

Completed.
