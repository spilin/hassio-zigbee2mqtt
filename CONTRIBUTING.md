# This repository

This fork only provides **extra Home Assistant add-on definitions** (metadata) that use the **official** Zigbee2MQTT image (`ghcr.io/zigbee2mqtt/zigbee2mqtt-{arch}`). There is **no** Docker build here.

Install **Zigbee2MQTT** from [zigbee2mqtt/hassio-zigbee2mqtt](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt), then add **this** repository for the extra instances (Garage, Apartment, Balcony, Gazebo, Attic, MC, Temp).

# Version bumps

When a new upstream Zigbee2MQTT add-on version is released (e.g. `2.10.0-1`):

1. Set the same `"version"` in each `zigbee2mqtt-*/config.json` (all seven add-on folders).
2. Prepend a line to each `CHANGELOG.md` under that version.
3. Commit to `master`.

The optional **Release** workflow (repository dispatch) can update all seven in one go if you use automation.

# Icons

See [ADDON_ASSETS.md](ADDON_ASSETS.md).
