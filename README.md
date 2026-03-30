<div align="center">
    <h1>Zigbee2MQTT — extra Home Assistant instances</h1>
    <p>Garage, apartment, balcony, gazebo, attic, mc, and temp add-ons using the <strong>official</strong> Zigbee2MQTT image.</p>
</div>

> [!CAUTION]
> If you're using a Raspberry Pi, use at least a Raspberry Pi 4; older models may be unstable for Zigbee2MQTT.

## What this is

- Install **Zigbee2MQTT** from the **official** repository: [zigbee2mqtt/hassio-zigbee2mqtt](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt).
- Add **this** repository in Home Assistant to install **additional** Zigbee2MQTT instances (each needs its own USB/network coordinator).
- All add-ons here use the same image as upstream: `ghcr.io/zigbee2mqtt/zigbee2mqtt-{arch}` — no separate Docker build in this repo.

### Port map (defaults)

| Add-on | Slug | Data path | Socat TCP | Web UI (host) |
|--------|------|-----------|-----------|---------------|
| **Zigbee2MQTT** (official) | `zigbee2mqtt` | `/config/zigbee2mqtt` | 8485 | 8099 / ingress |
| **Garage** | `zigbee2mqtt_garage` | `/config/zigbee2mqtt_garage` | 8486 | 8100 |
| **Apartment** | `zigbee2mqtt_apartment` | `/config/zigbee2mqtt_apartment` | 8487 | 8101 |
| **Balcony** | `zigbee2mqtt_balcony` | `/config/zigbee2mqtt_balcony` | 8488 | 8102 |
| **Gazebo** | `zigbee2mqtt_gazebo` | `/config/zigbee2mqtt_gazebo` | 8489 | 8103 |
| **Attic** | `zigbee2mqtt_attic` | `/config/zigbee2mqtt_attic` | 8490 | 8104 |
| **MC** | `zigbee2mqtt_mc` | `/config/zigbee2mqtt_mc` | 8491 | 8105 |
| **Temp** | `zigbee2mqtt_temp` | `/config/zigbee2mqtt_temp` | 8492 | 8106 |

Use a **different MQTT `base_topic`** for every instance.

### Icons

Put **`icon.png`** and **`logo.png`** in each add-on folder next to **`config.json`** — see **[ADDON_ASSETS.md](ADDON_ASSETS.md)**.

### Using this fork

1. Edit **`repository.json`** and set **`url`** to your GitHub repo.
2. If you ever point **`image`** at your own registry, update it in every add-on `config.json` in this repo (all seven folders).

## Installation

1. Install an MQTT broker if needed (e.g. **Mosquitto** from the Home Assistant add-on store).
2. Add the **official** Zigbee2MQTT repository and install **Zigbee2MQTT** from [here](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt).
3. **Add-on store → ⋮ → Repositories** — add **this** repository URL, then install any of **Garage**, **Apartment**, **Balcony**, **Gazebo**, **Attic**, **MC**, **Temp** as needed.
4. Start each add-on, open the web UI, complete onboarding, and assign a **unique** `base_topic` per instance.

More detail: [Zigbee2MQTT getting started](https://www.zigbee2mqtt.io/guide/getting-started/#onboarding).

## Changelogs

- [zigbee2mqtt-garage/CHANGELOG.md](zigbee2mqtt-garage/CHANGELOG.md)
- [zigbee2mqtt-apartment/CHANGELOG.md](zigbee2mqtt-apartment/CHANGELOG.md)
- [zigbee2mqtt-balcony/CHANGELOG.md](zigbee2mqtt-balcony/CHANGELOG.md)
- [zigbee2mqtt-gazebo/CHANGELOG.md](zigbee2mqtt-gazebo/CHANGELOG.md)
- [zigbee2mqtt-attic/CHANGELOG.md](zigbee2mqtt-attic/CHANGELOG.md)
- [zigbee2mqtt-mc/CHANGELOG.md](zigbee2mqtt-mc/CHANGELOG.md)
- [zigbee2mqtt-temp/CHANGELOG.md](zigbee2mqtt-temp/CHANGELOG.md)

## Issues

Problems with **devices or Zigbee2MQTT itself** → [Koenkk/zigbee2mqtt issues](https://github.com/Koenkk/zigbee2mqtt/issues).

Problems **specific to these add-on definitions** (ports, repo) → open an issue on **your** fork.

## Credits

- [zigbee2mqtt/hassio-zigbee2mqtt](https://github.com/zigbee2mqtt/hassio-zigbee2mqtt) — official Home Assistant add-on
- [Koenkk/zigbee2mqtt](https://github.com/Koenkk/zigbee2mqtt)
