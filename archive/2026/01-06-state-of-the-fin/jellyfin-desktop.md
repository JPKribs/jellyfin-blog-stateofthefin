---
client_name: Jellyfin Desktop
client_url: https://github.com/jellyfin/jellyfin-desktop
author_name: Andrew Rabert
author_url: https://github.com/andrewrabert
---

We're rebranding the desktop application from Jellyfin Media Player to Jellyfin Desktop.
The most noteworthy change is the migration from Qt 5 to Qt 6.
This seems to have improved overall performance, though we're still working out issues regarding memory leaks due to the migration.

Apart from the Qt migration, other noteworthy updates.

- Saved servers and settings will not be migrated from Jellyfin Media Player.
- We've laid the foundation for switching servers with the addition of profiles CLI options. The long-term goal is to have a UI for this as well, but the timeline is TBD.
- A slew of bug fixes are included.

The release is currently available on [Flathub](https://github.com/jellyfin/jellyfin-desktop) and in the [Arch Linux AUR](https://aur.archlinux.org/packages/jellyfin-desktop).
Stable builds for Windows and macOS builds are not currently available.
Other Linux distributions will likely be added, though we recommend using Flathub for the time being.
We are not currently supporting Ubuntu 24.04 LTS due to it being stuck on the older Qt 6.4 series, while our new dependency, mpvqt, requires at least Qt 6.5.
