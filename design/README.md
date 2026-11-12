# Neon city banner

The city background is an original generated illustration. `banner.html` renders the name as a neon sign and animates the surrounding light and its pavement reflections. The background, camera, and lettering stay still. There is no added rain, scrolling text, scanline, or flashing effect.

Preview from the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/design/banner.html`; append `?still` for a still frame. The preview also respects reduced-motion preferences.

The profile serves a full-colour animated WebP, a GIF fallback, and a static PNG for reduced-motion presentation. A direct static-image link is included below the profile text.

Palette: navy `#080D24`, cyan `#00E5FF`, magenta `#FF2AA1`, violet `#9254FF`, and pale text `#F3F6FF`. Typography: Orbitron for the name and monospace for the handle. Font licensing is included with the assets.

The five-second loop is rendered at 25 frames per second. The WebP encoder may coalesce visually identical frames while preserving their duration. The optional `window.exportBanner()` development helper posts 125 rendered PNG frames to a local `/__frame/NNN` export handler; it does not contact any third-party service and is not needed to view the banner.
