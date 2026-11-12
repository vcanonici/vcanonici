# Cyberpunk lightning banner

The original city artwork is kept intact. `banner.html` builds colour layers from the hue and saturation of the image itself, so every cyan/blue or pink/violet region responds together: buildings, sky, signs, and pavement reflections.

An eight-second loop starts in a darker low state. A blue lightning envelope raises luminance and shifts hue, fades out, then a pink envelope illuminates the matching regions. There is no decorative underline, drawn lightning bolt, artificial rain, or travelling scanline. The name and handle stay still and readable.

Preview from the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/design/banner.html`; append `?still` for a still image. Reduced-motion preferences also select a still frame.

The profile serves a full-colour animated WebP, a GIF fallback, and a static PNG for reduced-motion presentation. A direct static-image link is included below the profile text.

The main animation is rendered at 25 fps over eight seconds. The GIF fallback samples every other frame at 12.5 fps and uses a 900 × 300 render size to limit its download size. Encoders coalesce identical frames during the quiet intervals while preserving their duration. `window.exportBanner()` optionally posts 200 PNG frames to a local `/__frame/NNN` handler for encoding; it is not needed for viewing.

Palette: navy `#080D24`, cyan `#00E5FF`, magenta `#FF2AA1`, violet `#9254FF`, and pale text `#F3F6FF`. Typography: Orbitron for the name and monospace for the handle. Font licensing is included with the assets.
