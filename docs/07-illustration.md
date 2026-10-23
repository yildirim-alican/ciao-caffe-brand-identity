# 07 · Illustration & icons

All artwork is hand-built vector (inline SVG) — no stock images, no raster photos. That keeps the boards sharp at any size, lets every part animate, and keeps each screen file small.

## Drawing style

- **Line:** cream `#FFF8F1` outline, 7 px on the 400 × 440 product canvas (3.6–4 px on header icons, 1.8 px on 24 px UI icons), round caps and joins.
- **Fill:** flat colour, no gradients except inside the liquid (top-to-bottom, to show layers).
- **Glass:** body filled with cream at 12–14 % opacity, so the liquid is visible through it; a single highlight stroke at 35 % opacity.
- **Perspective:** a gentle three-quarter view — rims and surfaces are ellipses, so toppings can sit *on* the surface.

## Drinkware kit

| Vessel | Used for | Construction notes |
|---|---|---|
| Glass mug + saucer | hot lattes, signatures | tapered body 110→122 / 290→278 px, rim ellipse rx 90 ry 16; handle drawn **behind** the body so both ends tuck under its outline; rim split into back arc (behind liquid) and front arc (in front) |
| Turkish coffee cup + saucer | Türk kahvesi | opaque cup with red tulip band; coffee surface and foam rise inside the rim |
| Tall tumbler | all cold drinks | no straw; base liquid layer, ice that floats with the surface, boba resting on the bottom |
| Milk pitcher | lattes | rotated −55°; position solved so the spout tip sits exactly above the stream |
| Cezve | Turkish coffee | copper body, long wooden handle; spout tip placed above the cup centre |

The liquid is an HTML layer clipped by a polygon that matches the glass interior, so it can rise with a CSS transform while the outline SVG stays on top.

## Toppings (appear only after the pour)

latte-art star (Tarantino) · whipped cream with pistachio (Pistachio White Hot, steam disabled so it never crosses the cream) · caramel drizzle and a Lotus biscuit on the saucer (Lotus Latte) · strawberry (Ruby) · spice dust and a cinnamon stick (Cincirella) · milk swirl (Spanish Latte) · lemon wheel on the rim and mint on the surface (Berry Hibiscus Cooler) · coffee ice cubes (Kori Kohi).

## Header vectors

| Board | Vector | Motion |
|---|---|---|
| Hot | take-away cup with star sleeve | sway + steam |
| Cold | domed iced cup, no straw | ice bob + bubbles |
| Dessert | cupcake, symmetric around its centre axis: pleated wrapper, three frosting tiers, cherry — no ground line | float, cherry bob, sprinkle twinkle |

## UI icons

24 × 24, 1.8 px stroke, `currentColor`, one per section: espresso cup, take-away cup, Turkish cup, mug with heart, mug with cubes, tea glass, iced cup, bottle, shaker, boba cup, cake, dessert dome, sandwich, pizza slice. Size-legend icons: espresso cup (UNICO), small and large take-away cups (PICCOLO / GRANDE).

## The star

The star from the logo is the one shape repeated everywhere: list marks, badges, latte art, the rotating backdrop, sparkles. Path (24 × 24): `M12 2.5l2.8 6.1 6.6.7-5 4.5 1.4 6.6L12 17l-5.8 3.4 1.4-6.6-5-4.5 6.6-.7z`.
