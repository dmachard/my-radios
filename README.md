# My LiveRadio Stations

Personal backup of radio stations and logos for the [LiveRadio GNOME Shell extension](https://github.com/dmachard/gnome-shell-extension-liveradio).

## Structure

- `stations.json` — The list of stations (stream URLs, display names, and logo links).
- `icons/` — Radio station logos (PNG / SVG).

## Getting icons from Google Play

Open the app's icon on Google Play and copy its image URL. To choose the image resolution, change the size at the end of the URL: for example, replace `=s512` with `=s128`, `=s256`, or another size in pixels. For example, this icon URL requests a 512 × 512 image: [Google Play icon](https://play-lh.googleusercontent.com/zlDIMlYvey0oe2hJwOyMuMGO2hSdUDSR6Hy2PnpoM_aM_NV2AgEBAAFM7-mZZdDiFhhggNhLwn5e8G6D7IN8=s512). Download the image and save it in `icons/`.

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