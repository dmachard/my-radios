# My LiveRadio Stations

Personal backup of radio stations and logos for the [LiveRadio GNOME Shell extension](https://github.com/dmachard/gnome-shell-extension-liveradio).

## Structure

- `stations.json` — The list of stations (stream URLs, display names, and logo links).
- `icons/` — Radio station logos (PNG / SVG).

## Restore / Import into GNOME

### Option 1: Via command line (1-liner)

Run this command to import all stations into LiveRadio:

```bash
dconf write /org/gnome/shell/extensions/liveradio/radios "$(curl -sSL https://raw.githubusercontent.com/<YOUR_GITHUB_USERNAME>/my-radios/main/stations.json)"
```

### Option 2: Via GUI

Open LiveRadio preferences:

```bash
gnome-extensions prefs liveradio@dmachard.dev
```

Copy the content of stations.json and paste into the settings window and click Save.