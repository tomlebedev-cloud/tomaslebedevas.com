# tomaslebedevas.com

Asmeninis puslapis — vienas statinis HTML failas, be framework'ų, be build žingsnio, be npm.

## Failai

| Failas | Paskirtis |
|---|---|
| `index.html` | Visas puslapis: turinys, CSS ir 5 kalbų vertimai viename faile |
| `img/tomas-lebedevas.jpg` | Portretas, originalas (745×951), naudojamas kaip 2x |
| `img/tomas-lebedevas-portrait-480.jpg` | Portretas 4:5 (480×600) pirmam ekranui |
| `img/tomas-lebedevas-800.jpg` | Kvadratinis, nuorodų peržiūrai (`og:image`) |
| `robots.txt` | Leidžia indeksuoti, nurodo sitemap |
| `sitemap.xml` | Vienas įrašas — pagrindinis puslapis |

## Turinys ir dizainas

Skiltys: pirmas ekranas su portretu, „Apie" (viena pastraipa), knyga *The Reserve*,
keturios kortelės 2×2 (fotografija, šachmatai, sportas, asmeninis treneris) ir kontaktai
mėlynoje juostoje.
IT darbų sąrašas ir sertifikatai 2026-09-11 išimti — juos aprašo CV ir LinkedIn.

Spalvos paimtos iš portreto: balta, žydra (`--sky-*`) ir tamsiai mėlyna (`--navy`).
Tamsios temos nėra sąmoningai. Šriftai: Inter ir Source Serif 4 (knygos pavadinimui).

## Kalbos

EN · LT · ES · DE · FR. Vertimai yra `I18N` objekte `index.html` apačioje. Kalba
parenkama iš `localStorage`, jei nėra — iš naršyklės kalbos, jei ir tos nėra — EN.

Teksto keitimas: susirandi raktą (pvz. `book.lead`) ir taisai visose penkiose kalbose.
HTML'e tekstų nėra — tik `data-i18n` atributai.

## Ką dar reikia užpildyti

- YouTube ir Facebook nuorodos — HTML'e užkomentuotos, ties `URL-TODO`

Padaryta 2026-09-11: `The Reserve` aprašymas (`book.lead`, 5 kalbos) pagal rankraščio
paantraštę; reitingas `2030` sutampa su rankraščio „About the Author"; fotografijos nuorodos
nukreiptos į `tomaslebedevas.photography`; pridėti `canonical`, `og:url` ir pilnas `og:image` adresas.

## Deploy į GitHub Pages

```bash
git init
git add .
git commit -m "Personal site"
git branch -M main
git remote add origin https://github.com/tomlebedev-cloud/tomaslebedevas.com.git
git push -u origin main
```

Tada repo Settings → Pages → Source: `main` / `root`.

### Savas domenas

Kai domenas bus paruoštas, repo šaknyje sukurti `CNAME` failą su viena eilute:

```
tomaslebedevas.com
```

DNS registratoriuje:

- `A` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- Settings → Pages → Enforce HTTPS

## Peržiūra lokaliai

Atidaryti `index.html` naršyklėje. Nuotrauka rodoma tik tada, kai failas atidaromas
iš to paties katalogo (santykinis kelias `img/`).
