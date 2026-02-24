---
client_name: Jellyfin for Xbox
client_url: https://github.com/jellyfin/jellyfin-xbox
author_name: JPVenson
author_url: https://github.com/JPVenson
---

The last two updates brought the long awaited full gamepad support and fixes for 4K and HDR.

- **Gamepad support**: Gamepad navigation is now the default navigation type for the Jellyfin for Xbox app and requires a server version of 10.11 or higher to work. However as we cannot switch the input mode type while the app is running, the Jellyfin for Xbox app can no longer connect to older versions than 10.11. As this is a fundamental change in how the app works, there are still a few hiccups like the app not loading correctly and users reporting that the gamepad does not work at all. In those instances we recommend uninstalling and reinstalling the app.
- **Web UI TV mode**: For versions of Jellyfin earlier than 10.11.5 the web UI still runs in the desktop mode, which might look a bit odd. However, with Jellyfin 10.11.5, we have fixed a bug that now correctly sets the web UI to TV mode, so the UI should work a lot better.
- **4K and HDR**: For the last few versions, we have been working on enabling 4K and HDR for the app. This is done by integrating with the web UI and switching the HDMI modes. Sadly, this also comes at the cost of not being allowed to run in the background. To enable 4K support, we had to use a feature flag that allocates more video memory to the Jellyfin for Xbox app, making it incompatible with running in the background.
- **General Improvements**: Alongside the shiny new headline features, we have also been working on the code in general, adding small improvements and cleaning up a lot of code. The latest versions added log files and their upload to the Jellyfin server, tighter integrations with the web UI, a settings view that can be expanded for future features, version compatibility checking, a better server connection experience, and more.
- **Future**: When I took over the for the previous maintainer almost a year ago, I made a rough plan for the general development of the app. I always planned on keeping the app as a web wrapper because while the app is certainly more popular than most think, it does not have enough support in development to be a full UWP app. Nevertheless, there are a few features left on my to-do list:
  - Localization to other languages
  - Server discovery
  - Desktop support
  - Better decoder support
  - Subtitle storage on-device
