---
{
  "type": "web",
  "actors": [
    "user",
    "administrator"
  ],
  "entryPoints": [
    {
      "web": "/"
    },
    {
      "web": "/setup"
    },
    {
      "web": "/set-password"
    },
    {
      "web": "/admin"
    }
  ],
  "languages": [
    "de",
    "en",
    "cs",
    "fr",
    "it",
    "nl",
    "pl",
    "pt-BR",
    "ru",
    "sv",
    "es",
    "zh-CN"
  ],
  "references": [
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/index.html"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/static/js/app.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "web/sw.js"
    },
    {
      "kind": "code",
      "role": "implementation",
      "target": "api/main.py"
    }
  ]
}
---

# Web app

The app the server serves in the browser, installable as an offline-capable web app (PWA), with its first-run setup, password pages and administration area.
