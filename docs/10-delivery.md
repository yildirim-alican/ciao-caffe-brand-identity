# 10 · In-store delivery

What each store receives, and how it runs.

## Package

| Item | Format | Use |
|---|---|---|
| **Screen 1 — hot loop** | `screens/01_Ekran1_Sicak_Dongu.html` | left screen behind the counter |
| **Screen 2 — cold + dessert loop** | `screens/02_Ekran2_Soguk_Dongu.html` | right screen behind the counter |
| Alternative boards | `screens/03`–`07` | single-board layouts: hot/cold lists, desserts, image boards |
| Intros | `screens/08_Intro_Sicak.html`, `screens/09_Intro_Soguk.html` | brand intro on its own (events, social) |
| **Video fallback** | `video/*.mp4` — H.264, 1920×1080, 30 fps, 60 s | TVs without a browser (USB, repeat mode) |
| Stills | `previews/*.png` — 1920×1080 | approvals, print, social media |
| Drink panels | `previews/drinks/*.png` — 620×780 | product visuals on their own (social, print, web) |
| **Price list** | `menu/Ciao_Fiyat_Listesi.xlsx` | head office and till |

## Running the screens

1. Copy the two loop files to each screen's player (smart TV browser, mini PC, or stick).
2. Open the file and double-click for full screen.
3. Make sure both devices set their time automatically — that is all the two screens need to stay in step.

The files are fully offline: typefaces and logo are embedded, so nothing is loaded from the internet. The board scales itself to any resolution and aspect ratio, letterboxing when needed.

If a TV cannot open web pages, play the two MP4 files on repeat instead; start them together and the choreography matches the live version.

## Price list

| Sheet | Content |
|---|---|
| **Özet** | products, Ciao Selection count, price range and missing prices per board |
| **Sıcaklar · Soğuklar · Tatlı & Atıştırmalık** | printable lists in the board colours, with the logo; prices are entered here (blue) |
| **Tüm Ürünler (POS)** | flat list for the till; prices follow the board sheets automatically (green) |

Every sheet carries the logo top-left in a title band in the board colour and a narrow spacer column on the left. Prices that still need a value are highlighted in yellow; items not shown on screen (for example carton-cup Turkish tea) are noted.

## Keeping it consistent

Names, Ciao Selection marks and prices are the same on the screens, the featured product slides, the price list and the till list. A change to the menu is made once and carried through all of them before release.
