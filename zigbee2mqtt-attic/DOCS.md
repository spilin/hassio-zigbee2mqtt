# Zigbee2MQTT Attic (extra instance)

Uses the upstream image `ghcr.io/zigbee2mqtt/zigbee2mqtt-{arch}` with:

- Data directory default: `/config/zigbee2mqtt_attic`
- Published ports: socat **8490**, web UI on host **8104** (container frontend still listens on **8099**)

Set a **different MQTT `base_topic`** than your other Zigbee2MQTT instances.

## Socat default

```yaml
slave: tcp-listen:8490,keepalive,nodelay,reuseaddr,keepidle=1,keepintvl=1,keepcnt=5
```

See [zigbee2mqtt.io](https://www.zigbee2mqtt.io/) for general configuration.
