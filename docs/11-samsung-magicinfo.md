# 11 · Samsung MagicINFO

The menu boards run on Samsung commercial displays managed with **Samsung MagicINFO**. Each board is delivered as a ready-to-upload MagicINFO **web package**, with an MP4 alternative for displays that should play video instead.

## What to upload

| Display | Web package (primary) | Video (alternative) |
|---|---|---|
| **Screen 1** — hot drinks, red intro | [`magicinfo/web-packages/Ciao_Ekran1_Sicak.zip`](../magicinfo/web-packages/Ciao_Ekran1_Sicak.zip) | [`video/Ekran1_Sicak_Dongu_60sn.mp4`](../video/Ekran1_Sicak_Dongu_60sn.mp4) |
| **Screen 2** — cold drinks + desserts, blue intro | [`magicinfo/web-packages/Ciao_Ekran2_Soguk.zip`](../magicinfo/web-packages/Ciao_Ekran2_Soguk.zip) | [`video/Ekran2_Soguk_Dongu_60sn.mp4`](../video/Ekran2_Soguk_Dongu_60sn.mp4) |

Single-board packages for other layouts (lists, dessert board, image boards, intros) are in the same folder.

Every package contains one file, **`index.html`**, at the root of the ZIP. Fonts, logo, illustrations and animation are all inside that file, so the display needs **no internet connection** and loads nothing from outside. The board fills the display at 1920 × 1080 and scales itself to other resolutions (including UHD), letterboxing if the aspect ratio differs.

## Upload a web package

In MagicINFO Server:

1. **Content** › **Create** › **Upload Web Content**.
2. **Content name:** `Ciao – Ekran 1 Sıcak` (or `Ciao – Ekran 2 Soğuk`).
3. **Web Package:** select `index.html` and the matching ZIP from `magicinfo/web-packages/` (the HTML is also in [`screens/`](../screens)).
4. **Start Page:** `index.html`.
5. **Refresh Interval:** leave the default or set it long — the board runs continuously and never needs reloading. If a reload does happen, the loop continues from the right point, because it follows the clock rather than starting over.
6. **Save**, then repeat for the second screen.

## Schedule

1. Create two **device groups**: `Ciao · Ekran 1` (left display) and `Ciao · Ekran 2` (right display). MagicINFO publishes schedules to device groups.
2. **Schedule** › **Create Schedule** › **Content**, Schedule Type **General**, select the device type of your displays.
3. Add one program covering the full day:
   - content: the store's web package,
   - **Playing Time:** 24 hours,
   - **Repeat:** Everyday,
   - **Playback Date:** today, **Never expired**.
4. Publish one schedule to `Ciao · Ekran 1` with the hot package, and one to `Ciao · Ekran 2` with the cold package.

## Keeping the two screens in step

The two boards are designed as a pair: Screen 2 runs 30 seconds behind Screen 1, so the intros never play together and the dessert board only ever appears on one side. Each board works out its position from the **display's clock**, so the only requirement is that both displays show the same time:

- set both displays to the same **time zone** (Europe/Istanbul),
- enable **automatic time / NTP** on the displays (from the display menu or MagicINFO device control),
- keep both displays on the same network as the MagicINFO server.

No extra sync setting is needed for the web packages. Each board keeps its 30-second offset by itself, and each file already knows whether it is Screen 1 or Screen 2.

## Using the video alternative

Choose video when a display's built-in browser is older, or when the store prefers video content:

1. Upload the two MP4 files as normal content (H.264, 1920 × 1080, 30 fps, 60 s each).
2. Put each in a playlist on repeat and schedule it to its device group as above.
3. To keep the pair in step, use MagicINFO's synchronised playback for the two displays (both must be on the same network). The Screen 2 video is already shifted by 30 seconds, so starting both at the same moment reproduces the live choreography.

The video is a recording of the live board: same design, same timing. The only difference is that it repeats the same minute exactly, while the web package follows the clock.

## Display recommendations

- **Recent Samsung displays (Tizen-based SSSP models from roughly 2020 onward)** run the web packages smoothly. The boards use modern CSS animation (`clip-path`, SVG transforms) and are best on current firmware.
- **Older or entry-level models:** use the MP4 videos.
- Orientation: **landscape**, 16:9. Set picture mode to a standard or signage preset; avoid motion-smoothing options, which blur the pour animations.
- Before rollout to all stores, run each package for an hour on one display of every model in use.

## Updating prices

Price changes are made in the menu design and released as a new pair of packages. In MagicINFO, upload the new ZIP as a new version of the same web content, or replace the content in the schedule, and republish to both device groups. The price list in [`menu/`](../menu) is released alongside, so the till matches the screens.

---

### Türkçe kısa kurulum

1. **Content › Create › Upload Web Content** — `Ciao_Ekran1_Sicak.zip` (ve `index.html`) seçin, **Start Page:** `index.html`, kaydedin. Aynısını `Ciao_Ekran2_Soguk.zip` için yapın.
2. İki **cihaz grubu** oluşturun: *Ciao · Ekran 1* (sol) ve *Ciao · Ekran 2* (sağ).
3. Her gruba **24 saat · Her gün · Süresiz** bir zamanlama yayınlayın: Ekran 1'e sıcak, Ekran 2'ye soğuk paket.
4. İki ekranın **saat dilimi aynı** (İstanbul) ve **otomatik saat (NTP)** açık olsun. Ekranlar kendiliğinden 30 saniye kaydırmalı çalışır, ek ayar gerekmez.
5. Eski model ekranlarda web paketi yerine `video/` klasöründeki MP4'leri tekrar modunda oynatın.

*Menu paths follow the MagicINFO Server documentation ("Adding web content"; schedules and content synchronisation). Labels can differ slightly between MagicINFO versions.*
