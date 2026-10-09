# FLOW E-Checklist — Releases

Public Windows portable packages, SHA-256 checksums and release notes for FLOW E-Checklist. This repository is the download and in-app update endpoint; source development is maintained separately.

[Download the latest release](https://github.com/Disguise-Automation/Flow-E-Checklist-Releases/releases/latest)

## Install

1. Download `Flow-E-Checklist-Windows-x64.zip` from the latest release.
2. Extract it into a writable local folder. Node.js, Python and required Python libraries are included.
3. Double-click `start.cmd` and keep the terminal open.
4. Open `http://localhost:3000` on that computer. Other devices on the same network use its LAN IP address.

Configure HQ, CN, US, HK, JP or SK photo storage in FLOW's SC settings.

## Update

On the computer running FLOW, select **Updates / 软件更新 → Check GitHub / 检查 GitHub 更新 → Install and restart / 安装并重启**. Finish current work on connected devices before installing. Deployed computers need no GitHub account or token.

The updater verifies the package, preserves `.env`, `.storage-settings.json` and photos, backs up program files, and checks startup after restarting. Failed startup restores the previous version. Run through `start.cmd` for in-app installation.

Versions before v0.1.8 require a one-time manual upgrade: stop FLOW, extract the new package into a new folder, copy the existing `.env`, `.storage-settings.json` and local `uploads` folder, then run the new `start.cmd`. Check stored photo paths and existing photos before removing the old folder.

## Release assets

- `Flow-E-Checklist-Windows-x64.zip` — complete portable package.
- `Flow-E-Checklist-Windows-x64.zip.sha256` — SHA-256 checksum for manual verification.

The portable ZIP includes readable JavaScript/Python application files. Local configurations and photo data are not included in release assets.
