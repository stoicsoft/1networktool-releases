# 1NetworkTool releases

Installers and auto-update metadata for [1NetworkTool](https://1networktool.com), published by CI from the private desktop repository. Every macOS build is signed with a Developer ID and notarized by Apple.

**Download the latest version from [Releases](https://github.com/stoicsoft/1networktool-releases/releases/latest).**

## Which file do I need?

| Your machine | Download |
|---|---|
| Mac with Apple silicon (M1 and later) | `1NetworkTool-<version>-mac-arm64.dmg` |
| Mac with an Intel chip | `1NetworkTool-<version>-mac-x64.dmg` |
| Windows 10 / 11 (64-bit) | `1NetworkTool-Setup-<version>.exe` |

Not sure which Mac you have? Apple menu → About This Mac: "Chip: Apple M…" means arm64, "Processor: Intel" means x64.

## Auto-updates

The app checks this repository for new versions with [electron-updater](https://www.electron.build/auto-update) and asks before downloading anything. The `.zip`, `latest-mac.yml` and `latest.yml` files are for the updater; you don't need to download them.

## Headless nodes (Linux)

`1netd` (the daemon) and `1net` (the CLI) for Linux servers are attached to every release, for amd64 and arm64. The desktop app installs them on a VPS over SSH for you. To fetch one by hand, check it against `SHA256SUMS`:

```sh
curl -LO https://github.com/stoicsoft/1networktool-releases/releases/latest/download/1netd-linux-amd64
curl -LO https://github.com/stoicsoft/1networktool-releases/releases/latest/download/SHA256SUMS
sha256sum --check --ignore-missing SHA256SUMS
chmod +x 1netd-linux-amd64
```

## Licence

1NetworkTool is free to use, with Pro as a one-time purchase that includes 12 months of updates. Versions released inside your 12 months stay Pro forever. See [1networktool.com](https://1networktool.com).
