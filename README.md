# Plotwright: product page

The product page and documentation for **Plotwright 2.0**, a house builder for Blender 4.2+: draw houses wall by
wall in Build Mode, or generate complete houses and whole streets in one click. Version 2.0 brings **InteriorLab by
Voyde Procedural** inside (Blender 5.0+): furnish a room with one click, light the house with a real sun, and frame a
camera in every room. Houses export to Unreal Engine, Unity and Godot.

This repository holds only the description, the media and the docs. The add-on itself is sold on Superhive and is not
included here.

- Product page: `index.html`, at https://blenderprocedural.github.io/plotwright/
- Documentation: `docs.html`, at https://blenderprocedural.github.io/plotwright/docs.html
- `embed-preview.html` (not indexed): the page in iframes at the store's 832 px and 609 px description columns and at
  375 px, as Superhive shows it
- `images/`: the store images, the page images and the video posters; `images/v2/` and `media/v2/` hold the 2.0 stills,
  posters and loops; `media/`: the 1.0 feature loops and trailers; `plans/`: SVG floor plans exported by the add-on
- The product page loads Archivo, Barlow and Barlow Semi Condensed from Google Fonts (the docs load Archivo, Instrument
  Sans and IBM Plex Mono); nothing else comes from another site. If the fonts cannot load, local fallbacks sized to
  match stand in. `fonts/` (Inter) is no longer used by either page

## Embedding

Inside an iframe the page scales with the frame's width (the whole layout is in `rem`, and `1rem` is 1/52 of the
frame width), so its height is a fixed multiple of its width. Every section has a fixed height in `rem`, so fonts,
line breaks and interaction never change the page height. The `aspect-ratio` style keeps the iframe exactly as tall
as the page at any column width; `height` is only a fallback. Links to other pages open in a new tab, and the page
posts its height to the parent as `{type: "plotwright-height", height}`.

```html
<iframe src="https://blenderprocedural.github.io/plotwright/" title="Plotwright 2.0" width="100%" height="18400"
  frameborder="0" allowfullscreen="" style="width:100%;height:auto;aspect-ratio:832/18400;border:0;display:block"></iframe>
```

`18400` is the page height at 832 px (1150 rem). If a section's height (`--h` on each `section.sheet`) changes, the
sum of the `--h` values times 16 is the new height. Add `?embed=1` to the URL to preview the scaled layout outside an
iframe.

## License

All renders, videos, text and code in this repository are © BlenderProcedural. All rights reserved.
