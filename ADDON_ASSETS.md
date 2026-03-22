# Add-on `icon.png` and `logo.png`

Home Assistant Supervisor loads these from **the same directory as `config.json`** for each add-on (e.g. `zigbee2mqtt-gazebo/icon.png` next to `zigbee2mqtt-gazebo/config.json`).

| File | Purpose |
|------|---------|
| **`icon.png`** | Sidebar / small icon in the UI |
| **`logo.png`** | Add-on store and detail views |

Place both files in **each** add-on folder you use:

- `zigbee2mqtt-garage/`
- `zigbee2mqtt-apartment/`
- `zigbee2mqtt-balcony/`
- `zigbee2mqtt-gazebo/`
- `zigbee2mqtt-attic/`

You can use the same artwork as the [official Zigbee2MQTT add-on](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt/tree/master/zigbee2mqtt) or your own — commit them in this repo so the store shows them after you push.
