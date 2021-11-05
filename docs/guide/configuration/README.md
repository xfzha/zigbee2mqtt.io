---
next: adapter-settings.md
---

# Configuration

Zigbee2MQTT is configured using [YAML](https://en.wikipedia.org/wiki/YAML) based `configuration.yml` file.
The file have to be located in the `data` directory within your installation. The `data` directory and the `configuration.yml` has to be writeable for Zigbee2MQTT process because it can get updated - e.g. if you change the settings in the WebUI. It's possible specify a custom data directory by setting the `ZIGBEE2MQTT_DATA` environment variable.

```yaml
# Minimal configuration.yml example
permit_join: true
mqtt:
  base_topic: zigbee2mqtt
serial:
  port: /dev/ttyUSB0
frontend:
  port: 8080
```

::: tip CONVENTION
The _dot-notation_ of a config-key like `mqtt.server` means `server` property within the `mqtt`
section. All _dot-notation_ references are absolute.
:::

## Environment variables

It is possible to override the values in `configuration.yaml` via environment variables. The name of the environment
variable should start with `ZIGBEE2MQTT_CONFIG_` followed by the path to the property you want to set in uppercase split
by a `_`.

In case you want to for example override:

```yaml
mqtt:
  base_topic: zigbee2mqtt
```

set `ZIGBEE2MQTT_CONFIG_MQTT_BASE_TOPIC` to the desired value.

## Config changes at runtime

Some configuration options can be changed at runtime by issuing a MQTT-publish at the topic `zigbee2mqtt/bridge/request/options`.
See [MQTT Topics and Messages](../usage/mqtt_topics_and_messages.md#zigbee2mqtt-bridge-request) for details.
