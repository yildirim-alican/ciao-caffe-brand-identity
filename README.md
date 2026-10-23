<p align="center">
  <img src="brand/logo/ciao-logo.png" alt="Ciao logo" width="260">
</p>

<h1 align="center">Ciao Caffè — Franchise Brand Identity & Digital Menu System</h1>

<p align="center">
  Corporate franchise identity, in-store digital menu boards, signature drink naming and motion design<br>
  for <a href="https://ciaocaffe.net">Ciao Caffè</a> · designed by <b>Alican Yıldırım</b>
</p>

<p align="center">
  <img src="assets/readme/hero-hot.gif" alt="Screen 1 — hot drinks loop" width="49%">
  <img src="assets/readme/hero-cold.gif" alt="Screen 2 — cold drinks loop" width="49%">
</p>

---

## Project

A complete identity and menu system for a coffee franchise, designed as a system rather than a single poster: one visual language that runs across two simultaneous in-store screens, a printable price list and the till's product list.

| | |
|---|---|
| **Client** | Ciao Caffè — [ciaocaffe.net](https://ciaocaffe.net) |
| **Scope** | Brand identity system · logo usage · digital menu boards (2 × 1920×1080) · motion & illustration · signature drink naming · dessert naming · price list |
| **Design** | Alican Yıldırım — brand, UI/UX, illustration, motion, naming, front-end |
| **Year** | 2026 |
| **Status** | In use in store |

## Highlights

- **Two screens that work as a pair.** Screen 1 loops *intro → hot drinks* (60 s, seven featured drinks). Screen 2 loops *intro → cold drinks → desserts* (60 s). Each opens with an intro in its own colour — red for hot, blue for cold. Both follow the device clock, so two independent screens stay in step without a server, and the dessert board never competes with itself.
- **Motion that tells the product story.** A pitcher or *cezve* arrives and pours from its spout into the centre of the glass, the liquid rises with ripples, ice falls and floats, toppings land on the surface, steam rises — then it rests. Every animation is physically logical and nothing passes through anything else. See [docs/06-motion.md](docs/06-motion.md).
- **A naming system.** Italian size names (UNICO · PICCOLO · GRANDE); the *Ciao Signature* drink line; *Ciao Selection* for barista picks; *Ciao Duetto* for dessert × coffee pairings; and a dessert list renamed after cinema, stage and art — Noir, Altın Lotus, Kuğu Gölü, Moulin Rouge, Roma Tatili… — with the original product name kept underneath for staff.
- **One menu, everywhere.** Names, Ciao Selection marks and prices on the screens match the price list and the till list exactly.
- **Built for Samsung MagicINFO.** Each screen ships as a ready-to-upload MagicINFO web package — one offline `index.html` with fonts and logo inside — scheduled 24/7 to its own device group. A 60-second MP4 of each loop is included as a video alternative. See [docs/11-samsung-magicinfo.md](docs/11-samsung-magicinfo.md).

## Inside

```
.
├── brand/
│   ├── logo/          Ciao logo + usage notes
│   ├── fonts/         Barlow Condensed · Kaushan Script · Permanent Marker (with licences)
│   └── tokens/        colours, type scale, layout and motion values (JSON · CSS)
├── docs/              the design system, one topic per file (start at 01)
├── magicinfo/         Samsung MagicINFO web packages (ZIP, index.html start page)
├── screens/           the menu boards as offline HTML — open in any browser
├── previews/          stills of every board and every product slide
├── video/             60-second loops of both screens (MP4, 1080p)
├── menu/              price list (Excel) — per-board sheets, summary, till list
└── assets/readme/     images for this page
```

## Design system

| | |
|---|---|
| [01 · Brand overview](docs/01-brand-overview.md) | positioning, personality, voice, sub-brands |
| [02 · Logo](docs/02-logo.md) | construction, clear space, minimum size, backgrounds, misuse |
| [03 · Colour](docs/03-color.md) | three board themes, neutrals, illustration palette |
| [04 · Typography](docs/04-typography.md) | three typefaces, roles, type scale, Turkish characters |
| [05 · Components](docs/05-components.md) | every building block of the boards |
| [06 · Motion](docs/06-motion.md) | pour/fill timeline, transitions, ambient loops, easing |
| [07 · Illustration & icons](docs/07-illustration.md) | vector drinkware, toppings, header vectors, icon set |
| [08 · Menu & naming](docs/08-menu-system.md) | sizes, Ciao Signature, Ciao Selection, Ciao Duetto, dessert names |
| [09 · Screen loops](docs/09-screen-loops.md) | two-screen choreography and timing |
| [10 · In-store delivery](docs/10-delivery.md) | what the store receives and how it runs |
| [11 · Samsung MagicINFO](docs/11-samsung-magicinfo.md) | uploading, scheduling and syncing the two displays |

## Gallery

### Screens

<table>
<tr><td width="50%" align="center"><img src="previews/Ekran1_b_icecek_1.png" width="100%" alt="Screen 1 · hot loop"><br><sub>Screen 1 · hot loop</sub></td><td width="50%" align="center"><img src="previews/Ekran2_b_icecek_1.png" width="100%" alt="Screen 2 · cold loop"><br><sub>Screen 2 · cold loop</sub></td></tr>
<tr><td width="50%" align="center"><img src="previews/03_Sicak_Liste.png" width="100%" alt="Hot list board"><br><sub>Hot list board</sub></td><td width="50%" align="center"><img src="previews/04_Soguk_Liste.png" width="100%" alt="Cold list board"><br><sub>Cold list board</sub></td></tr>
<tr><td width="50%" align="center"><img src="previews/Ekran2_c_tatli.png" width="100%" alt="Desserts & snacks"><br><sub>Desserts & snacks</sub></td><td width="50%" align="center"><img src="previews/06_Sicak_Gorselli_5.png" width="100%" alt="Hot board · image panel"><br><sub>Hot board · image panel</sub></td></tr>
<tr><td width="50%" align="center"><img src="previews/Ekran1_a_intro.png" width="100%" alt="Intro · hot"><br><sub>Intro · hot</sub></td><td width="50%" align="center"><img src="previews/Ekran2_a_intro.png" width="100%" alt="Intro · cold"><br><sub>Intro · cold</sub></td></tr>
</table>

### Hot drinks

Each featured drink pours, fills and is served in its own short animation; these are the final frames.

<table>
<tr><td width="25%" align="center"><img src="previews/drinks/hot-01-tarantino.png" width="100%" alt="Tarantino"><br><sub>Tarantino</sub></td><td width="25%" align="center"><img src="previews/drinks/hot-02-pistachio-white-hot.png" width="100%" alt="Pistachio White Hot"><br><sub>Pistachio White Hot</sub></td><td width="25%" align="center"><img src="previews/drinks/hot-03-lotus-latte.png" width="100%" alt="Lotus Latte"><br><sub>Lotus Latte</sub></td><td width="25%" align="center"><img src="previews/drinks/hot-04-damla-sakizli-turk-kahvesi.png" width="100%" alt="Damla Sakızlı Türk Kahvesi"><br><sub>Damla Sakızlı Türk Kahvesi</sub></td></tr>
<tr><td width="25%" align="center"><img src="previews/drinks/hot-05-ruby.png" width="100%" alt="Ruby"><br><sub>Ruby</sub></td><td width="25%" align="center"><img src="previews/drinks/hot-06-cincirella.png" width="100%" alt="Cincirella"><br><sub>Cincirella</sub></td><td width="25%" align="center"><img src="previews/drinks/hot-07-spanish-latte.png" width="100%" alt="Spanish Latte"><br><sub>Spanish Latte</sub></td><td width="25%"></td></tr>
</table>

### Cold drinks

<table>
<tr><td width="25%" align="center"><img src="previews/drinks/cold-01-kori-kohi.png" width="100%" alt="Kori Kohi"><br><sub>Kori Kohi</sub></td><td width="25%" align="center"><img src="previews/drinks/cold-02-tarantino-iced.png" width="100%" alt="Tarantino"><br><sub>Tarantino</sub></td><td width="25%" align="center"><img src="previews/drinks/cold-03-iced-spanish-latte.png" width="100%" alt="Iced Spanish Latte"><br><sub>Iced Spanish Latte</sub></td><td width="25%" align="center"><img src="previews/drinks/cold-04-taro-milk-boba-tea.png" width="100%" alt="Taro Milk Boba Tea"><br><sub>Taro Milk Boba Tea</sub></td></tr>
<tr><td width="25%" align="center"><img src="previews/drinks/cold-05-berry-hibiscus-cooler.png" width="100%" alt="Berry Hibiscus Cooler"><br><sub>Berry Hibiscus Cooler</sub></td><td width="25%"></td><td width="25%"></td><td width="25%"></td></tr>
</table>

## View it

- **In store:** upload [`magicinfo/web-packages/Ciao_Ekran1_Sicak.zip`](magicinfo/web-packages/Ciao_Ekran1_Sicak.zip) and [`Ciao_Ekran2_Soguk.zip`](magicinfo/web-packages/Ciao_Ekran2_Soguk.zip) to Samsung MagicINFO as web content (start page `index.html`) — [setup guide](docs/11-samsung-magicinfo.md).
- **On a computer:** download [`screens/01_Ekran1_Sicak_Dongu.html`](screens/01_Ekran1_Sicak_Dongu.html) or [`screens/02_Ekran2_Soguk_Dongu.html`](screens/02_Ekran2_Soguk_Dongu.html) and open it in a browser (GitHub shows the source, not the page). Double-click for full screen.
- **As video:** [`video/`](video).

## Türkçe özet

Ciao Caffè için hazırlanmış kurumsal franchise marka kimliği ve dijital menü sistemi. Ekranlar Samsung MagicINFO ile yönetilir; her ekran için hazır web paketi (ZIP, başlangıç sayfası `index.html`) ve alternatif MP4 video teslim edilir. İki ekran aynı anda çalışır: **Ekran 1** kırmızı intro + sıcaklar, **Ekran 2** mavi intro + soğuklar + tatlı. İkisi de 60 saniyelik döngüdür ve cihaz saatine göre birlikte ilerler. Ürün görsellerinde döküm, dolum, buz ve buhar animasyonları vardır. Boy isimleri UNICO · PICCOLO · GRANDE; imza içecekler *Ciao Signature*, barista seçimleri *Ciao Selection*, tatlı–kahve eşleşmeleri *Ciao Duetto* olarak adlandırıldı. Tatlılar sinema, sahne ve sanattan, ürünü doğrudan çağrıştıran isimler aldı. Marka sistemi, isimlendirme, illüstrasyon, animasyon ve ekran tasarımı **Alican Yıldırım**'a aittir.

## Credits

**Alican Yıldırım** — brand identity system, logo application, UI/UX and menu board design, illustration, motion design, signature drink and dessert naming, front-end.
[github.com/yildirim-alican](https://github.com/yildirim-alican)

## Licence

**All rights reserved.** This repository is public so the work can be reviewed; it is **not** open source. See [LICENSE](LICENSE) and [NOTICE.md](NOTICE.md).
