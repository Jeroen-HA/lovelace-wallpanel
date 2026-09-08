# WallPanel
[![hacs_badge](https://img.shields.io/badge/HACS-Default-41BDF5.svg?style=for-the-badge)](https://github.com/hacs/integration)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/j-a-n/lovelace-wallpanel?style=for-the-badge)](https://github.com/j-a-n/lovelace-wallpanel/releases)
[![GitHub stars](https://img.shields.io/github/stars/j-a-n/lovelace-wallpanel?color=yellow&style=for-the-badge)](https://github.com/j-a-n/lovelace-wallpanel/stargazers)
![GitHub All Releases](https://img.shields.io/github/downloads/j-a-n/lovelace-wallpanel/total.svg?color=green&style=for-the-badge)
[![Documentation](https://img.shields.io/badge/view-Documentation-blue?style=for-the-badge)](https://j-a-n.github.io/lovelace-wallpanel/ "Go to WallPanel documentation")

🖼️ **Wall panel mode for your Home Assistant Dashboards.**  

WallPanel is a configurable extension that features:
- Photo and video slideshow screensaver
- Show dashboard views, cards and badges of your choice on top of the images.
- Full-screen mode
- Hide the side and or top bar 
- Screen wake lock
- Motion detection

You can use images and videos from the following sources:
- Home Assistant Media-source
- Immich
- Home Assitant entities with entity_picture attribute
- Full websites as iframe
- Unsplash

![Screenshot of screensaver](./docs/screensaver-screenshot.png)

## 🔧 About this fork

This is a personal fork of [j-a-n/lovelace-wallpanel](https://github.com/j-a-n/lovelace-wallpanel) currently testing two additional features, both intended to eventually be proposed upstream as separate pull requests once validated on real hardware:

- **Immich portrait pairing** — completes the existing `immich_combine_portraits` config option (already present upstream but not yet functional) by adding the missing rendering logic: two portrait photos from an Immich album are composited side-by-side into a single landscape slide. Related upstream issue: [#514](https://github.com/j-a-n/lovelace-wallpanel/issues/514) (also being addressed independently via [#581](https://github.com/j-a-n/lovelace-wallpanel/pull/581) for Media-source images).
- **Night mode** — a new `night_mode_entity` option that dims the screensaver or switches to a black screen with a live clock, driven by any Home Assistant entity (e.g. a light/illuminance sensor going dark).

Status: actively testing on a wall-mounted tablet. Not yet submitted upstream.

## Installation
* Search for `WallPanel` in the Home Assistant Community Store
* Click on the repository
* Click the `Download` button
* You can now select a special version if required
* Click on `Download`

## Quick Start
After [Installation](#installation) you can enable wallpanel for a dashboard.
To do this, add a wallpanel configuration to your Home Assistant dashboard configuration yaml (raw config).

* Navigate to the dashboard.
* Click Overview in your sidebar.
* Click the three dots menu (top-right) and click on Edit Dashboard.
* Click the three dots menu again and click on Raw configuration editor.
* Add the `wallpanel` configuration above anything else.

```yaml
wallpanel:
  enabled: true
  hide_toolbar: false
  hide_sidebar: true
  fullscreen: false
  idle_time: 10
```

After saving and closing the dashboard configuration, WallPanel should now be active for this dashboard.
The sidebar should be hidden and the screensaver should start after an idle time of 10 seconds.

## Documentation
Further information can be found in the [WallPanel Documentation](https://j-a-n.github.io/lovelace-wallpanel/).
