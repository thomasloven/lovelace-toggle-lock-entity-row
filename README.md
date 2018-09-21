toggle-lock-entity-row
======================

Avoid toggling entities by mistake in lovelace.

This will display a normal toggle with a lock symbol in front of it.
Clicking the lock will make it go away and enable the toggle to be manouvered for five seconds.

---
```yaml
resources:
  - url: /local/toggle-lock-entity-row.js
    type: js

views:
  - title: My view
    cards:
    - type: entities
      entities:
        - entity: light.my_lamp
          name: A lamp
          type: custom:toggle-lock-entity-row
```

![lovelace-locked-toggle](https://user-images.githubusercontent.com/1299821/45876486-0bc76e80-bd9b-11e8-8aa1-543fa4e3d14d.jpg)
