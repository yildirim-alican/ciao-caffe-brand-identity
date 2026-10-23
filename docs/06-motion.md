# 06 · Motion

Motion on a menu board has one job: draw the eye to what the brand wants to sell, then get out of the way. Every animation here follows three rules:

1. **It must be physically logical.** Liquid leaves the spout and lands in the centre of the glass; ice floats; toppings sit on the surface; steam only appears once the drink is poured.
2. **It must finish.** Product stories complete in ≈ 5 s and then rest; only small ambient loops keep running.
3. **Nothing collides.** Moving elements never pass through each other; the backdrop star stays clear of the product area.

All motion is pure CSS (`@keyframes`), so it runs on any browser, including TV browsers, without JavaScript animation libraries.

## The pour → fill → serve timeline (each product slide)

| Time (s) | What happens | Keyframes · easing |
|---|---|---|
| 0.0 – 0.6 | slide fades/scales in (0.96 → 1) | `ciSlide` · ease-out |
| 0.15 – 1.2 | (cold) ice cubes fall into the empty glass, one after another | `ciIce` · cubic-bezier(.55,0,.8,.3) — gravity |
| 0.3 – 0.9 | pitcher / cezve slides in from top-right, already tilted, spout over the glass centre | `ciJug` 4.7 s · ease-in-out |
| 0.9 – 4.3 | stream grows from the spout, stays, then fades | `ciStrm` · scaleY from the top |
| 1.0 – 4.3 | liquid rises inside a clip-path shaped like the glass interior; surface ellipse rises with it; ice rises with the surface | `ciFillH` / `ciFillC` 3.3 s · cubic-bezier(.3,.55,.35,1) |
| 1.0 – 4.3 | ripples spread where the stream hits the surface (×6) | `ciRip` 0.55 s · linear |
| 4.3 – 5.0 | pitcher leaves the frame | end of `ciJug` |
| 4.4 – 5.1 | toppings pop onto the surface (latte-art star, cream, drizzle, garnish) | `ciPop` 0.7 s · back-out |
| 5.0 → | steam rises (hot), bubbles rise (soda), drops run down the glass (cold), ice bobs | `ciSteam2`, `ciFz`, `ciDrp`, `ciBob2` loops |

Because each slide is mounted fresh, the whole story replays every time the slide appears.

## Transitions

| Transition | Duration | How |
|---|---|---|
| Slide → slide | 0.6 s | new slide mounts with `ciSlide` (opacity + scale) |
| Scene → scene (intro / drinks / desserts) | 0.7 s | `ciScene` opacity fade |
| Intro | 5.0 s | a circle in the screen's colour (red on Screen 1, blue on Screen 2) wipes open (`ciaoBg`, clip-path circle), logo pops with overshoot, tag line rises, six stars pop and vanish, circle closes |

## Ambient loops

| Element | Keyframes | Period | Notes |
|---|---|---|---|
| Ciao Selection stars | `ciStar` | 3.6 s | scale 1 → 1.55 + 24° turn + glow, then settle; staggered by 0.55 s per star |
| Signature cards | `sigWave` | 4 s | 14 px hop, 0.12 s apart → a wave |
| Ciao Duetto pairings | `sigWave` | 5 s | 0.3 s apart |
| Header cup (hot) | `ciSway` + `ciSteam` | 4.2 s / 2.4 s | cup sways ±3°, three steam lines rise in turn |
| Header glass (cold) | `ciBob` + `ciFizz` | 2.6 s / 2.2 s | ice cubes bob, bubbles rise |
| Header cupcake (dessert) | `ciFloat` + `ciBob2` + `ciStar` | 4 s / 3 s | cupcake floats, cherry bobs, sprinkles twinkle |
| Backdrop star | `ciSpin` | 80 s | one large star at the band/panel corner, rotating; small stars twinkle in free band space only |
| Spotlight illustration | `ciFloat` | 4 s | 8 px float |

## Principles for new animations

- Use `transform` and `opacity` only (GPU-friendly, smooth on TV hardware).
- For SVG parts, set `transform-box: fill-box` and an explicit origin; never animate an element that already has a `transform` attribute — wrap it in a `<g>` first.
- Keep ambient loops ≥ 2 s and subtle; keep story animations ≤ 5 s.
- Stagger repeated elements so the screen never "blinks" as a whole.
