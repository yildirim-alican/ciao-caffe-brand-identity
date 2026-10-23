# 10 · In-store delivery

What each store receives, and how it runs.

## Package

| Item | Format | Use |
|---|---|---|
| **Screen 1 — hot loop** | `magicinfo/web-packages/Ciao_Ekran1_Sicak.zip` (+ `screens/01_Ekran1_Sicak_Dongu.html`) | left display, via Samsung MagicINFO |
| **Screen 2 — cold + dessert loop** | `magicinfo/web-packages/Ciao_Ekran2_Soguk.zip` (+ `screens/02_Ekran2_Soguk_Dongu.html`) | right display, via Samsung MagicINFO |
| Alternative boards | `screens/03`–`07` | single-board layouts: hot/cold lists, desserts, image boards |
| Intros | `screens/08_Intro_Sicak.html`, `screens/09_Intro_Soguk.html` | brand intro on its own (events, social) |
| **Video alternative** | `video/*.mp4` — H.264, 1920×1080, 30 fps, 60 s | displays that should play video content |
| Stills | `previews/*.png` — 1920×1080 | approvals, print, social media |
| Drink panels | `previews/drinks/*.png` — 620×780 | product visuals on their own (social, print, web) |
| **Price list** | `menu/Ciao_Fiyat_Listesi.xlsx` | head office and till (incl. Simpra setup sheet) |
| **Price labels** | `labels/*.pdf` — A4 sheets with crop marks and single 80 × 50 mm pages; `labels/png/` 300 dpi | display case, counter and bar front (25 labels) |

## Running the screens

The displays are Samsung commercial screens managed with **Samsung MagicINFO**. Upload each ZIP as *Web Content* (start page `index.html`), schedule it 24 hours a day to its device group, and keep both displays on automatic time. Step-by-step instructions: [11 · Samsung MagicINFO](11-samsung-magicinfo.md).

The packages are fully offline: typefaces and logo are embedded, so nothing is loaded from the internet. Each board scales itself to the display's resolution. Displays that should play video instead use the two MP4 files.

## Price list

| Sheet | Content |
|---|---|
| **Özet** | products, Ciao Selection count, price range and missing prices per board |
| **Sıcaklar · Soğuklar · Tatlı & Atıştırmalık** | printable lists in the board colours, with the logo; prices are entered here (blue) |
| **Kasa Önü** | counter items not on the screens (mini cookies) and the labelled bar-front drinks |
| **Tüm Ürünler (POS)** | flat list for the till; prices follow the board sheets automatically (green) |
| **Simpra Menü** | one row per till button: menu group, sub-group, POS name, portion (UNICO / PICCOLO / GRANDE / Tek), price, where it is sold, whether it has a label |

Every sheet carries the logo top-left in a title band in the board colour and a narrow spacer column on the left. Prices that still need a value are highlighted in yellow; items not shown on screen (for example carton-cup Turkish tea) are noted.

## Keeping it consistent

Names, Ciao Selection marks and prices are the same on the screens, the featured product slides, the price list and the till list. A change to the menu is made once and carried through all of them before release.
