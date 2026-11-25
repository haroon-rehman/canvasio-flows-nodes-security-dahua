# Dahua Device

Canvas IO Workflows — maintained integration/fork of an independent Node-RED node package.

## Canvas IO

| | |
|--|--|
| Domain | Security / Dahua |
| Development status | Integrated in local harness (canvasio-flows-dev) |
| Palette category (operational) | `Canvas IO` |
| Config nodes | remain `category: "config"` |
| Local repository | `canvasio-flows-nodes/canvasio-flows-node-security-dahua` |
| npm package name | `@canvasio/node-security-dahua` (`1.0.3-canvasio.1`); lineage tag `v1.0.3` |

`canvasio-flows-nodes` is an organizational parent only — not a monorepo. One node package = one Git repository.

This repository is a **Canvas IO-maintained integration/fork**. Protocol and node runtime logic originate from upstream; Canvas IO changes are limited to integration, presentation, and local development packaging.

## Nodes

### Operational (palette: Canvas IO)

- `dahua-device`, `dahua-device-day`, `dahua-device-night`

### Configuration

- `dahua-device-config`

## Development

```powershell
cd C:\GitHub\canvasio\canvasio-flows\canvasio-flows-nodes\canvasio-flows-node-security-dahua
npm install
```

Local harness:

```powershell
cd C:\GitHub\canvasio\canvasio-flows\canvasio-flows-dev
npm install
cd C:\GitHub\canvasio\canvasio-flows\canvasio-flows-core
node packages/node_modules/node-red/red.js --userDir C:\GitHub\canvasio\canvasio-flows\canvasio-flows-dev
```

Open http://localhost:1880

## Testing

No automated unit tests.

## Upstream

| | |
|--|--|
| Original package | `node-red-contrib-dahua-device` |
| Upstream project | https://github.com/inwaar/node-red-contrib-dahua-device |

Canvas IO does not claim authorship of the original upstream implementation.

## License

MIT (see package.json; add LICENSE file in a later hygiene pass if missing).

---

## Upstream documentation

The following sections retain useful upstream technical documentation (adapted only where needed).

node-red-contrib-dahua-device
========================

![NPM status](https://img.shields.io/npm/v/node-red-contrib-dahua-device)
![Node-RED status](https://img.shields.io/badge/dynamic/xml?label=Node-RED%20catalog&query=%2F%2Fdiv%5B%40class%3D%27flowmeta%27%5D%5B1%5D%2Fdiv%5B%40class%3D%27flowinfo%27%5D%5B1%5D%2Ftext%28%29%5B1%5D&url=https%3A%2F%2Fflows.nodered.org%2Fnode%2Fnode-red-contrib-dahua-device)
![Github Actions status](https://img.shields.io/github/actions/workflow/status/inwaar/node-red-contrib-dahua-device/release.yml?label=release)

Provides a node for grabbing Dahua DVR/NVR (digital video recorder) or IP-camera events like
<code>VideoMotion</code>, <code>AlarmLocal</code>, <code>VideoLoss</code> and <code>VideoBlind</code>.</p>

Additionally it provides nodes to set Day or Night profile.

Supports digest authentication for the last Dahua firmware devices.

Pre-requirements
-------

<details><summary>Debian based operation systems</summary>

    sudo apt-get install build-essential git

</details>
<details><summary>Hass.io</summary>

https://github.com/inwaar/node-red-contrib-dahua-device/issues/4#issuecomment-602093620

</details>
<details><summary>Other operation systems</summary>

follow instructions https://github.com/nodejs/node-gyp#on-unix

</details>

Install
-------

Run the following command in your Node-RED user directory - typically `~/.node-red`

    npm i node-red-contrib-dahua-device

Usage
-----

Configure motion detection on a Dahua device. Drop the Dahua device node to a flow. 

If you want to trigger day or night profile, drop the Dahua device day / night node to a flow.

Example
-------
![example](./images/example.png)
