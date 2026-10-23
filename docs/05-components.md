# 05 · Components

Every board is assembled from the same parts. Sizes are for a 1920 × 1080 canvas.

## Layout frames

| Frame | Structure |
|---|---|
| **List board** (`Main`, `Soguk`) | 184 px header band → 3-column list grid (64 px gutters) → Signature card row → footer (extras + legend) |
| **Image board** (`Sicak_Medya`, `Soguk_Medya`, loop screens) | 156 px full-width band → 620 px image panel + 2-column list. Band and panel are **one continuous L-shaped surface** (no divider), with the backdrop star turning at their corner |
| **Dessert board** (`Tatlilar`) | 184 px band → 2-column list + Ciao Duetto row → 560 px *Ciao Selection* panel on the right, again one L-shaped surface with the band |

## Header band

Logo (left) · animated vector + board title in Kaushan + rotated sticker slogan (centre) · size legend or ticket badge (right).

## Size legend

Icon + name + volume for each size the board uses:
`UNICO — Tek ölçü` (hot only) · `PICCOLO — 12 oz · 350 ml` · `GRANDE — 16 oz · 470 ml`.
The cold boards have no single-size drinks, so UNICO is omitted there.

## Section header

Line icon (24 px, 1.8 stroke) + UPPERCASE title in the theme accent + right-aligned column labels, on a 1.5 px rule.

## Price rows

| Variant | Grid |
|---|---|
| `r` — two sizes | `1fr 70–74px 72–82px` → name · PICCOLO · GRANDE |
| `r1` — one price | `1fr 138–156px` → name · UNICO |
| Multi-serving | one line, options pushed right: `Türk Çayı ……… Bardak 70 TL · Fincan 90 TL` |

A row is: **name** (Barlow 600) → optional ★ → **description** (muted, 15–16 px) → prices with `TL`.

## Ciao Selection star

A 15 px star after the item name, in the theme accent. It twinkles on a staggered schedule so the board shimmers instead of blinking at once ([06 · Motion](06-motion.md)).

## Signature row

A rotated *Ciao Signature* sticker (Kaushan + 3D drop shadow) followed by 4–5 cards: name, optional `YENİ` tag, description (list boards), PICCOLO/GRANDE prices stacked label-over-number. Cards bob in a wave, 0.12 s apart.

## Ferahlatıcılar strip (cold)

A single line of water, soda, lemonade and energy drink with one price each, between two rules. On the 3-column list it spans **only the first two columns**, ending where they end.

## Image panel slide

`badge` (CIAO SIGNATURE / CIAO SELECTION / YENİ TAT) → **400 × 440 illustration** → product name (Kaushan) → ingredients → price pill (`PICCOLO 290 TL · GRANDE 320 TL`). Under it: progress dots (one per slide) and a corner note: ★ *Ciao Selection* · *Fiyatlar KDV dahildir*.

## Dessert rows

Stage name (28 px bold) · optional ★ · original name in gold + ingredients · price, or a gold **YAKINDA** tag for items not yet on sale.

## Ciao Duetto

One rounded card above the footnote rule: *Kahvenin yanına* in Kaushan with `CIAO DUETTO` below, then four pairings separated by hairlines. Each pairing shows a cake-slice icon, the dessert name, and `+ coffee` in gold underneath: *Noir + Espresso*, *Altın Lotus + Lotus Latte*, *Copacabana + Türk Kahvesi*, *Roma Tatili + Espresso*. Pairings bob gently in a staggered wave.

## Ticket badge

A cinema ticket (dark body, dashed inner outline, two punched notches in the band colour) with a twinkling star: **SAHNEDE BUGÜN — Günün tatlıları vitrinde rol almaya hazır**. It ties the dessert board to its cinema/stage naming.

## Ciao Selection panel (dessert)

Badge → floating product illustration → stage name (80 px Kaushan) → original name + ingredients → price chip.
