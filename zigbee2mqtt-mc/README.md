# Home Assistant App: Zigbee2MQTT MC

[![Docker Pulls](https://img.shields.io/docker/pulls/zigbee2mqtt/zigbee2mqtt-amd64.svg?style=flat-square&logo=docker)](https://hub.docker.com/r/zigbee2mqtt/zigbee2mqtt-amd64)

Same Zigbee2MQTT image as the **official** add-on, as an **extra instance** with its own coordinator and config.

- Default **data path**: `/config/zigbee2mqtt_mc`
- Default **host ports**: socat **8491**, frontend **8105**
- **`icon.png`** and **`logo.png`** in this folder (next to `config.json`) are used by the Supervisor store.

Install the main **Zigbee2MQTT** from the [official repository](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt), then add this repository for additional instances. Use a **unique MQTT `base_topic`** per instance.

See [Zigbee2MQTT docs](https://www.zigbee2mqtt.io/).
