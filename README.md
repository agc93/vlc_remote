[![hacs_badge](https://img.shields.io/badge/HACS-Custom-orange.svg?style=for-the-badge)](https://github.com/agc93/vlc_remote)

# Remote VLC Media Control Component

Home Assistant custom component using VLC's HTTP API for controlling a remote instance of VLC Media Player.

> Enable HTTP interface in VLC before setting up this component, taking note of username/password and configured port.

## Installation

#### Option 1: (recommended)
This repository is compatible with the Home Assistant Community Store ([HACS](https://community.home-assistant.io/t/custom-component-hacs/121727)).

After installing HACS, add this repo as a custom repository from the Settings screen, and use the ```configuration.yaml``` example below.

#### Option 2: (manual)

Download this repository as a zip file, and place the vlc_remote directory in your config/custom_components/ directory.

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
    
## Changelog

- Initial version borrowed heavily from Squeezebox setup by Kingo55.
- Added play_media url option by gambalaya (required for HA text to speech).
- HACS-friendly repo changes by agc93

To Do:
 - Async
 - Syncing
 - More media info and typing
 - Handle closing/stop states better
