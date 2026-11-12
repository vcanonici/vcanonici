# Cyberpunk lightning banner

The profile displays `assets/banner.svg`. The original city is stored as three lossless PNG layers inside the SVG; blue and pink light animate through their opacity. Lettering is made from vector glyph outlines, with a constant glow. There is no text rasterization, video compression, or GIF palette in the displayed banner.

The eight-second loop uses cubic Bézier easing for a gradual rise and decay. Blue rises over 650 ms and fades over 1550 ms; pink rises over 750 ms and fades over 1600 ms. The camera and lettering stay still. There is no decorative underline or artificial rain.

The README selects a static PNG when reduced motion is requested. A direct static-image link is included below the profile text. Older WebP/GIF exports remain as historical assets and are not used to display the profile.

`banner.html` contains the source colour-layer preparation and a canvas preview. To preview locally, serve the repository root:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open `http://127.0.0.1:8000/design/banner.html`; append `?still` for a still image. `window.exportLayers()` can post the three prepared layers to a local export handler as PNGs 200–202. The SVG embeds those layers and uses native animation rather than storing a sequence of compressed frames.

Palette: navy `#080D24`, cyan `#00E5FF`, magenta `#FF2AA1`, violet `#9254FF`, and pale text `#F3F6FF`. Lettering uses outlines from Orbitron, whose license is included with the font assets.
