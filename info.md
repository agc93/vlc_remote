# Remote VLC Media Control Component

Home Assistant custom component using VLC's HTTP API for controlling a remote instance of VLC Media Player.

> Enable HTTP interface in VLC before setting up this component, taking note of username/password and configured port.

## Configuration

Configure according to the following example and restart Home Assistant.

```yaml
media_player:
  - platform: vlc_remote
    host: 192.168.0.x
    port: 8080
    name: "HTPC VLC" # Optional
    username: "something" # Optional
    password: "xyz" # Optional
```