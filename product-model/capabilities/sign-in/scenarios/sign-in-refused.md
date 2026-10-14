---
{
  "kind": "validation",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The User enters a username or email and a password that do not match an account",
      "kind": "actor",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      }
    },
    {
      "text": "The Product refuses with the same message whether the account exists or the password is wrong",
      "kind": "product",
      "actor": "user",
      "entities": [],
      "contexts": {
        "web": {
          "place": "web-app::sign-in::sign-in"
        }
      }
    }
  ]
}
---

# Sign in with wrong credentials

## Trigger

A person mistypes their password or username.

## Outcome

Nobody is signed in and the message does not reveal whether the account exists.
