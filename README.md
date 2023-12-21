# Mattermost Desktop - Flatpak

## Native Wayland support and Fractional scaling under Wayland

Wayland support has already been implemented but disabled by default due to rendering issues. A simple reload (Ctrl+R) fixes these errors.

You can enable it with [Flatseal](https://flathub.org/apps/com.github.tchx84.Flatseal) by checking the "Wayland windowing system" toggle or by running the command below:

```bash
flatpak override -u com.mattermost.Desktop --socket=wayland
```

## Development

### Prerequisites

```bash
flatpak install flathub org.freedesktop.Sdk//22.08
flatpak install flathub org.electronjs.Electron2.BaseApp//22.08
```

### Build to locally and run

```bash
flatpak-builder --user --install --force-clean build-dir com.mattermost.Desktop.json
flatpak run com.mattermost.Desktop
```
