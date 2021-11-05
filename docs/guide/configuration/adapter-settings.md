---
sidebarDepth: 1
---

# Adapter settings

Configuration of the Zigbee USB-Adapter.  
You can use `dmesg` command on Linux hosts to find the mounted device.

```yaml
# Required: serial settings
serial:
  # Required: location of the adapter (e.g. CC2531).
  # To autodetect the port, set 'port: null'.
  port: /dev/ttyACM0
  # Optional: disable LED of the adapter if supported (default: false)
  disable_led: false
  # Optional: adapter type, not needed unless you are experiencing problems (default: shown below, options: zstack, deconz, ezsp)
  adapter: null
```

<!-- TODO: some notes about rtscts? Is it useful, which adapter supports it? -->
```yaml
advanced:
  # Optional: Baud rate speed for serial port, this can be anything firmware support but default is 115200 for Z-Stack and EZSP, 38400 for Deconz, however note that some EZSP firmware need 57600.
  baudrate: 115200
  # Optional: RTS / CTS Hardware Flow Control for serial port (default: false)
  rtscts: false
  # Optional: soft reset ZNP after timeout (in seconds); 0 is disabled (default: 0)
  soft_reset_timeout: 0
  # Optional: configure adapter concurrency (e.g. 2 for CC2531 or 16 for CC26X2R1) (default: null, uses recommended value)
  adapter_concurrent: null
```

::: tip 
It's also possible to connect Adapters over TCP. See how to connect a [remote adapter](../../advanced/remote-adapter/connect_to_a_remote_adapter.md).
:::


## Transmitter power

```yaml
experimental:
  # Optional: Transmit power setting in dBm (default: 5).
  # This will set the transmit power for devices that bring an inbuilt amplifier.
  # It can't go over the maximum of the respective hardware and might be limited
  # by firmware (for example to migrate heat, or by using an unsupported firmware).
  # For the CC2652R(B) this is 5 dBm, CC2652P/CC1352P-2 20 dBm.
  transmit_power: 5
```


