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
          unlockdelay: 5
          unlockcolor: '#00ff00'
          relockdelay: 2
          users:
            - Thomas
            - Admin
```

## Options

| Name | Type | Default | Description
| ---- | ---- | ------- | -----------
| users | list | none | Users which can disabled lock **\*\***
| unlockdelay | int | 0 | Time it takes for the lock to be removed
| relockdelay | int | 5 | Time it takes the switches to be locked again
| unlockcolor | hex | '#000000' | Icon color 

![lovelace-locked-toggle](https://user-images.githubusercontent.com/1299821/45876486-0bc76e80-bd9b-11e8-8aa1-543fa4e3d14d.jpg)

**\*\*** Note that this is not to be considered propper security. The lock can easily be circumvented.
