# tomaslebedevas.com

Asmeninis puslapis — vienas statinis HTML failas, be framework'ų, be build žingsnio, be npm.

## Failai

| Failas | Paskirtis |
|---|---|
| `index.html` | Visas puslapis: turinys, CSS ir 5 kalbų vertimai viename faile |
| `img/tomas-lebedevas.jpg` | Portretas (745×951) |
| `robots.txt` | Leidžia indeksuoti, nurodo sitemap |
| `sitemap.xml` | Vienas įrašas — pagrindinis puslapis |

## Kalbos

EN · LT · ES · DE · FR. Vertimai yra `I18N` objekte `index.html` apačioje. Kalba
parenkama iš `localStorage`, jei nėra — iš naršyklės kalbos, jei ir tos nėra — EN.

Teksto keitimas: susirandi raktą (pvz. `book.lead`) ir taisai visose penkiose kalbose.
HTML'e tekstų nėra — tik `data-i18n` atributai.

## Ką dar reikia užpildyti

- `The Reserve` aprašymas — dabar tik „knyga, kurią šiuo metu rašau" (raktas `book.lead`)
- YouTube ir Facebook nuorodos — HTML'e užkomentuotos, ties `URL-TODO`
- Šachmatų reitingas `2030` — patikrinti, ar teisingas (`index.html`, sekcija `#chess`)

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
