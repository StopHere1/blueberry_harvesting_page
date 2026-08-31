# blueberry_harvesting_page

Project page for the [Autonomous Blueberry Harvester](https://github.com/StopHere1/autonomous_blueberry_harvester)
— a 6-DOF harvesting arm with a current-based, force-aware rolling gripper and a
vision-guided perception pipeline.

**Live site:** https://stophere1.github.io/blueberry_harvesting_page/

## Layout

| Path | Purpose |
| --- | --- |
| `index.html` | The entire site — self-contained HTML, inline CSS/JS, inline SVG. No build step. |
| `media/` | Images and video referenced by the figure slots. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is instead of running Jekyll. |

## Editing

Edit `index.html` and open it in a browser to preview. Push to `main` and Pages
redeploys within a minute or so.

## Filling the figure slots

The page has six `<figure class="fig">` blocks holding placeholders. Each one
contains an HTML comment with the exact tag to paste in. Drop the asset into
`media/`, then swap the inner `<div class="ph">…</div>` for the real element:

```html
<img src="media/workspace.png" alt="Voxel map of the reachable workspace">
<video src="media/demo.mp4" controls muted loop playsinline poster="media/demo-poster.jpg"></video>
```

The wrapper handles sizing and the caption bar, so the asset just needs a sane
aspect ratio — 16:9 for the demo and workspace slots, 4:3 for the paired ones.
**Delete any slot you do not fill** before publishing; an unfilled placeholder
renders as a visible hatched box.

## Publishing setup

Settings → Pages → Build and deployment → **Deploy from a branch**, branch
`main`, folder `/ (root)`.
