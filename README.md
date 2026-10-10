# Megtalálnak – weboldal

Egyszerű, statikus weboldal (HTML + CSS), nincs szükség szerverre vagy adatbázisra.
Bármilyen tárhelyre feltölthető, vagy ingyen futtatható GitHub Pages / Netlify / Cloudflare Pages alatt.

## Mappák

```
index.html            főoldal
adatvedelem.html      adatkezelési tájékoztató (minta, kitöltendő)
minta/                3 mintaoldal kitalált vállalkozásoknak (referenciának)
assets/css/style.css  a főoldal stílusa
assets/fonts/         betűtípusok (saját tárhelyről, nem a Google-től)
assets/img/           képek, ikon
robots.txt, sitemap.xml
```

## Élesítés előtt kitöltendő

Minden kitöltendő rész szögletes zárójelben van, és az oldalon sárgával ki van emelve.
Keress rá a `[` jelre a fájlokban:

- `[ÁR]` – a három csomag ára
- `[ÁFA-TARTALOM]`, domain/tárhely díj
- `[IDŐTARTAM]` – mennyi idő alatt készül el
- `[NÉV]`, `[TELEPÜLÉS]`, `[TELEFONSZÁM]`, `[E-MAIL]`
- impresszum: `[VÁLLALKOZÓ NEVE]`, `[CÍM]`, `[ADÓSZÁM]`, `[EV-SZÁM]`
- `[DOMAIN]` – index.html (ld+json), robots.txt, sitemap.xml
- a telefonos linkekben (`href="tel:[TELEFONSZÁM]"`) a szám szóközök nélkül, pl. `tel:+36301234567`

A "Megtalálnak" munkanév: használat előtt nézd meg, szabad-e a domain és nem használja-e más.

A fotód helyét az index.html-ben a `portrait` rész jelöli: tegyél egy képet az `assets/img/` mappába,
és cseréld a `<span>Ide jön a fotód</span>` részt egy `<img src="assets/img/foto.webp" alt="...">` sorra.

## Ajánlatkérő űrlap bekötése

Statikus oldalon az űrlapnak kell egy fogadó szolgáltatás. A legegyszerűbb a Formspree (ingyenes csomag van):

1. Regisztrálj, hozz létre egy űrlapot, kapsz egy címet, pl. `https://formspree.io/f/abcd1234`.
2. Az index.html-ben a `data-endpoint=""` részbe írd be ezt a címet.

Netlify-on helyette a beépített Netlify Forms is használható.

## Feltöltés GitHub Pages-re

1. Hozz létre egy új repository-t a GitHubon.
2. Töltsd fel ennek a mappának a teljes tartalmát.
3. Settings → Pages → Branch: `main`, mappa: `/ (root)` → Save.
4. Saját domainhez: Settings → Pages → Custom domain, és a domain DNS-ében állítsd be a GitHub által kért rekordokat.

## Fotók

A mintaoldalak fotói a Pexelsről származnak (ingyenesen használhatók, üzleti célra is),
és közvetlenül a Pexels szerveréről töltődnek be. Ha biztosra akarsz menni, töltsd le őket
az `assets/img/` mappába, és írd át a `https://images.pexels.com/...` címeket a helyi fájlra.

A főoldal "Munkáim" részében a mintaoldalak élő, kicsinyített előnézete látszik.
Ha ez valahol nem tölt be, alatta egy képernyőkép jelenik meg helyette.
