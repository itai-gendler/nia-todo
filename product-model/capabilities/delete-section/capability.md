---
{
  "availability": [
    {
      "place": "web-app::app"
    }
  ],
  "domain": "projects",
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/routers/sections.py"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/features/section-actions.js"
    }
  ]
}
---

# Delete section

A person deletes a section; its todos move to Unsorted in the same project.
