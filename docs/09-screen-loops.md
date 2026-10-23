# 09 · Screen loops

Two 1920 × 1080 screens run side by side behind the counter.

## Choreography

| | 0 – 5 s | 5 – 40 s | 40 – 60 s |
|---|---|---|---|
| **Screen 1 — hot** | intro | hot drinks · 7 featured drinks, 55 s ÷ 7 ≈ 7.9 s each (runs to 60 s) | ← |
| **Screen 2 — cold** | intro | cold drinks · 5 featured drinks × 7 s | desserts (20 s) |

Each screen opens with the intro in its own colour — **red** for hot, **blue** for cold. Screen 2 is shifted by **30 seconds**, so the intros never play at the same time and the guest always has a full drinks board in view.

```
time  0        10        20        30        40        50        60
S1   [I][ hot · Tarantino → Pistachio → Lotus → Damla → Ruby → Cincirella → Spanish ]
S2   [ cold ......... ][ desserts ......... ][I][ cold · Kori → Tarantino → … ]
```

Desserts hold the screen for at most 20 s per minute; drinks keep the rest.

## How sync works without a server

Each loop computes its position from the device clock:

```js
t = ((Date.now() / 1000 + faz) % 60 + 60) % 60
scene = t < 5 ? 'intro' : t < drinkEnd ? 'drinks' : 'desserts'
slide = floor((t - 5) / ((drinkEnd - 5) / slides))
```

`faz` is 0 for Screen 1 and 30 for Screen 2 (overridable with `?faz=` in the URL). Any two devices with automatic time set stay aligned to well under a second. No network, CMS or controller is needed.

## Featured slides

| Screen 1 (hot) | Screen 2 (cold) |
|---|---|
| Tarantino · Pistachio White Hot · Lotus Latte · Damla Sakızlı Türk Kahvesi · Ruby · Cincirella · Spanish Latte | Kori Kohi · Tarantino · Iced Spanish Latte · Taro Milk Boba Tea · Berry Hibiscus Cooler |

Slide prices always match the list prices, so the featured price and the list never disagree.

## Video fallback

For TVs without a browser, [`video/`](../video) holds 60-second MP4 recordings of both loops (H.264, 1080p, 30 fps). The Screen 2 video is pre-rotated by 30 s, so starting both files together reproduces the live choreography. Set the TV to repeat.
