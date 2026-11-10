# Neon city banner

The city background is an original generated illustration. `banner.html` renders the typography, breathing neon lights, and rain on a canvas. The animation uses a four-second loop; the lettering stays still.

Preview from the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/design/banner.html`; append `?still` for a still frame. The profile uses the checked-in GIF, with a static PNG for reduced-motion presentation and a direct link to the static version.

Palette: navy `#080D24`, cyan `#00E5FF`, magenta `#FF2AA1`, violet `#9254FF`, and pale text `#F3F6FF`. Typography: Orbitron for the name and monospace for the handle. Font licensing is included with the assets.

The optional `window.exportBanner()` development helper posts forty rendered PNG frames to a local `/__frame/NNN` export handler. It does not contact a third-party service and is not needed to view the banner. The committed GIF contains forty frames at 100 ms each.
