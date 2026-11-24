# Plotwright: product page

The product page and documentation for **Plotwright**, a modular house builder for Blender 4.2+: draw houses wall by
wall in Build Mode, or generate complete houses and whole streets in one click; add roofs, stairs, dormers, chimneys,
balconies and bay windows; restyle and paint them; and export them to Unreal Engine, Unity and Godot with LODs and
collision.

This repository holds only the description, the media and the docs. The add-on itself is sold on Superhive and is not
included here.

- Product page: `index.html`, at https://blenderprocedural.github.io/plotwright/
- Documentation: `docs.html`, at https://blenderprocedural.github.io/plotwright/docs.html
- `images/`: the store images, the page images and the video posters; `media/`: the feature loops and the trailer;
  `plans/`: SVG floor plans exported by the add-on
- Inter is bundled in `fonts/`, so the pages make no external requests

## Embedding

Inside an iframe the page scales with the frame's width (the whole layout is in `rem`, and `1rem` is 1/52 of the
frame width), so its height is a fixed multiple of its width. The `aspect-ratio` style keeps the iframe exactly as tall
as the page at any column width; `height` is only a fallback. Links to other pages open in a new tab, and the page
posts its height to the parent as `{type: "plotwright-height", height}`.

```html
<iframe src="https://blenderprocedural.github.io/plotwright/" title="Plotwright" width="100%" height="HEIGHT"
  frameborder="0" style="width:100%;height:auto;aspect-ratio:832/HEIGHT;border:0;display:block"></iframe>
```

`HEIGHT` is the page height at 832 px. Add `?embed=1` to the URL to preview the scaled layout outside an iframe.

## License

All renders, videos, text and code in this repository are © BlenderProcedural. All rights reserved.
