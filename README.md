# Mattermost Desktop - Flatpak

## Prerequisites

```
$ flatpak install flathub org.freedesktop.Sdk//20.08
$ flatpak install flathub org.electronjs.Electron2.BaseApp//20.08
```

## Build to local repository, install

```
$ flatpak-builder build-dir com.mattermost.Desktop.json --force-clean --repo=repo
$ flatpak --user remote-add --no-gpg-verify test-repo repo
$ flatpak --user install test-repo com.mattermost.Desktop
```

