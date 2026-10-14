---
{
  "scope": "The FastAPI server, the web app and the native app shells.",
  "method": "Static inspection of source, migrations, translations and documentation at the pinned commit; nothing was executed.",
  "covered": [
    {
      "description": "Server routes and services for accounts, workspaces, projects, sections, sharing, todos, places, reminders, push and administration.",
      "paths": [
        "api/routers/auth.py",
        "api/routers/me.py",
        "api/routers/setup.py",
        "api/routers/password_setup.py",
        "api/routers/workspaces.py",
        "api/routers/projects.py",
        "api/routers/sections.py",
        "api/routers/sharing.py",
        "api/routers/todos.py",
        "api/routers/places.py",
        "api/routers/reminders.py",
        "api/routers/push.py",
        "api/routers/admin.py",
        "api/routers/instance.py",
        "api/routers/websocket.py",
        "api/main.py",
        "api/services/"
      ]
    },
    {
      "description": "Database schema migrations.",
      "paths": [
        "api/migrations/"
      ]
    },
    {
      "description": "Web app pages, features, offline sync and translations.",
      "paths": [
        "web/index.html",
        "web/admin.html",
        "web/setup.html",
        "web/set-password.html",
        "web/sw.js",
        "web/manifest.json",
        "web/static/js/",
        "web/static/i18n/"
      ]
    },
    {
      "description": "Native reminder, location reminder and server connection code of the desktop and Android apps.",
      "paths": [
        "src-tauri/src/",
        "src-tauri/gen/android/app/src/main/java/"
      ]
    }
  ],
  "exclusions": [
    {
      "description": "Tests and developer scripts.",
      "paths": [
        "scripts/"
      ]
    },
    {
      "description": "Packaging, service units, CI and build tooling.",
      "paths": [
        "packaging/",
        "systemd/",
        ".github/",
        "src-tauri/gen/android/buildSrc/",
        "src-tauri/gen/schemas/",
        "src-tauri/capabilities/",
        "src-tauri/permissions/",
        "start.sh",
        "package.json",
        "package-lock.json"
      ]
    },
    {
      "description": "Styles, icons, vendored libraries and bundled release notes.",
      "paths": [
        "web/static/css/",
        "web/static/style.css",
        "web/static/icons/",
        "web/static/vendor/",
        "web/static/content/",
        "web/downloads/"
      ]
    },
    {
      "description": "Native app build configuration, manifests and resources.",
      "paths": [
        "src-tauri/Cargo.toml",
        "src-tauri/Cargo.lock",
        "src-tauri/build.rs",
        "src-tauri/tauri.conf.json",
        "src-tauri/icons/",
        "src-tauri/linux/",
        "src-tauri/windows/",
        "src-tauri/gen/android/app/src/main/res/",
        "src-tauri/gen/android/app/src/main/AndroidManifest.xml",
        "src-tauri/gen/android/app/build.gradle.kts",
        "src-tauri/gen/android/app/proguard-rules.pro",
        "src-tauri/gen/android/build.gradle.kts",
        "src-tauri/gen/android/settings.gradle",
        "src-tauri/gen/android/gradle.properties",
        "src-tauri/gen/android/gradle/",
        "src-tauri/gen/android/gradlew",
        "src-tauri/gen/android/gradlew.bat"
      ]
    },
    {
      "description": "Repository metadata and legal notices.",
      "paths": [
        "README.md",
        "CONTRIBUTING.md",
        "SECURITY.md",
        "LICENSE",
        "NOTICE"
      ]
    },
    {
      "description": "Developer documentation and the changelog.",
      "paths": [
        "docs/",
        "CHANGELOG.md"
      ]
    },
    {
      "description": "Server process plumbing: database access, migration runner, request middleware, rate limits and command-line helpers.",
      "paths": [
        "api/db.py",
        "api/migrate.py",
        "api/middleware/",
        "api/rate_limit.py",
        "api/run_server.py",
        "api/change_admin_password.py",
        "api/set_trusted_proxies.py",
        "api/paths.py",
        "api/errors.py",
        "api/__init__.py",
        "api/routers/__init__.py"
      ]
    }
  ],
  "unmapped": [
    {
      "description": "Two-factor authentication, passkeys, trusted devices and device sessions, for users and in administration.",
      "paths": [
        "api/routers/two_factor.py",
        "web/static/js/features/security-dialogs.js"
      ]
    },
    {
      "description": "OIDC single sign-on and its administration.",
      "paths": [
        "api/routers/oidc.py",
        "web/static/js/pages/oidc-completion.js",
        "web/static/js/pages/oidc-native-return.js"
      ]
    },
    {
      "description": "BrainDump voice capture and its administration.",
      "paths": [
        "api/routers/braindump_v2.py",
        "web/static/js/features/braindump-live.js"
      ]
    },
    {
      "description": "Server updates, technical statistics and the administration overview.",
      "paths": [
        "api/routers/server_updates.py",
        "web/static/js/features/server-update-indicator.js"
      ]
    },
    {
      "description": "Desktop integration: global hotkeys, tray and app settings; app downloads and the native update prompt.",
      "paths": [
        "web/static/js/features/desktop-integration.js",
        "web/static/js/features/app-downloads.js",
        "web/static/js/features/desktop-hotkey-descriptions.js"
      ]
    },
    {
      "description": "The dashboard statistics endpoint used by API clients.",
      "paths": [
        "api/routers/dashboard.py"
      ]
    },
    {
      "description": "Personal view toggles (Today and Calm views, sorting, theme), keyboard shortcuts, search and the What's new dialog.",
      "paths": [
        "web/static/js/features/view-preferences.js",
        "web/static/js/features/theme.js",
        "web/static/js/features/shortcut-help.js",
        "web/static/js/features/mobile-search.js",
        "web/static/js/features/whats-new.js"
      ]
    }
  ],
  "limitations": []
}
---

# Coverage
