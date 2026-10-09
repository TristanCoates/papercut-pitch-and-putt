# PaperCut Pitch & Putt

Six holes of office mini golf that run in the browser, with real 2D rigid-body physics from [Matter.js](https://brm.io/matter-js/) 0.19.0 (MIT).

**Play it:** https://tristancoates.github.io/papercut-pitch-and-putt/

## How to play

Drag back from anywhere on the course and let go to putt. The further you pull, the harder the shot. Works with a mouse or a finger.

| Hole | Name | Par | Hazard |
|---|---|---|---|
| 1 | The Print Queue | 2 | A paper stack in the way |
| 2 | Follow-Me Release | 3 | S-bend |
| 3 | Toner Spill | 3 | Toner slows the ball right down, bouncy bumper |
| 4 | Paper Jam | 3 | Spinning blade that knocks the ball about |
| 5 | Coffee Break | 3 | Coffee spill (+1 stroke, back to where you shot from) and a sliding printer |
| 6 | The Last Page | 4 | Angled banks, bumpers and toner |

## Physics

- Zero-gravity top-down world, fixed 60 Hz step independent of screen refresh rate
- Rolling resistance via air friction, higher on toner
- Wall restitution 0.75, bumpers 1.15 (they add energy)
- Spinner and sliding printer are kinematic bodies, so they transfer their real velocity to the ball on contact
- The cup only takes a ball moving slowly enough; a fast ball lips out, a near miss gets pulled in by the lip

## Run locally

No build step. Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8000
```
