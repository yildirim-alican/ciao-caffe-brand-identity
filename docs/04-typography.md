# 04 · Typography

Three typefaces, each with one job. All three cover the full Turkish character set (ç ğ ı İ ö ş ü) via their *latin-ext* subsets.

| Typeface | Role | Weights |
|---|---|---|
| **Kaushan Script** | display: board titles (*Sıcaklar*, *Soğuklar*, *Tatlı & Atıştırmalık*), featured product names, *Signature*, *Kahvenin yanına* | 400 |
| **Barlow Condensed** | everything functional: section titles, item names, descriptions, prices, labels, badges | 400 · 500 · 600 · 700 · 800 |
| **Permanent Marker** | sticker slogans and the intro tag line (*Sıcacık bir ciao!*, *More Coffee More Life*) | 400 |

Why condensed? A menu board is a table seen from three metres away. A condensed sans keeps long names ("Iced Cappuccino Affogato", "Double Damla Sakızlı Türk Kahvesi") on one line, while the tall x-height keeps them readable.

## Type scale (1920 × 1080)

| Style | Font | Size / weight | Tracking | Example |
|---|---|---|---|---|
| Board title | Kaushan | 62–76 px | 0 | *Sıcaklar* |
| Featured name | Kaushan | 52–80 px | 0 | *Tarantino* |
| Sticker slogan | Permanent Marker | 22–26 px, rotated −3° | .02em | Sıcacık bir ciao! |
| Section title | Barlow 800 | 22 px, UPPERCASE | .14em | ESPRESSO BAR |
| Column label | Barlow 700 | 14 px, UPPERCASE | .08–.10em | PICCOLO · GRANDE |
| Item name | Barlow 600 | 21–25 px | 0 | Flat White |
| Item description | Barlow 400 | 15–18 px, `mute` | .02em | Yoğun espresso · Süt |
| Price | Barlow 600–700, tabular figures | 21–34 px | 0 | 250 |
| Currency | Barlow 700 | 0.58 em of the price, 72 % opacity | .04em | TL |
| Badge | Barlow 800 | 18 px, UPPERCASE, pill | .16em | CIAO SELECTION |

## Rules

- Prices always use **tabular figures** (`font-variant-numeric: tabular-nums`) so columns align.
- `TL` follows every price, smaller and lighter, so the number stays the hero.
- Ingredient lists are separated with a middle dot `·`, never commas.
- Dessert rows show two names: the **stage name** large, the **original product name** in the accent colour below (*Noir* / **Brownie**). Guests read the story, staff find the product.
- Never set body copy in Kaushan or Permanent Marker.

Font files and licences: [`brand/fonts/`](../brand/fonts).
