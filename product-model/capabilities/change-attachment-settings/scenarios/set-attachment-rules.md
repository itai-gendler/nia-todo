---
{
  "kind": "primary",
  "routes": {
    "web": "Web"
  },
  "steps": [
    {
      "text": "The Administrator turns uploads on or off, lists the allowed file types and sets the default storage per person",
      "kind": "actor",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Attachments enabled",
            "Allowed attachment types",
            "Default attachment quota"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::attachments"
        }
      }
    },
    {
      "text": "The Product saves them for every upload from now on",
      "kind": "product",
      "actor": "administrator",
      "entities": [
        {
          "entity": "instance-settings",
          "effect": "changes",
          "facts": [
            "Attachments enabled",
            "Allowed attachment types",
            "Default attachment quota"
          ]
        }
      ],
      "contexts": {
        "web": {
          "place": "web-app::administration::attachments"
        }
      }
    }
  ]
}
---

# Change the attachment settings

## Trigger

The household wants to attach Office documents too.

## Outcome

Uploads follow the new rules; existing attachments stay.

## Edge cases

- At least one allowed type is required.
