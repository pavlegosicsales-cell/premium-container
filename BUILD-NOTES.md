# Premium Container, beleške o buildu

Sajt je napravljen Skillom 02 (`website-build-rules`) iz `context.md`, a dizajn je
preuzet iz vašeg prethodnog builda `github.com/pavlegosicsales-cell/kiwiseal-roofing`
(live: kiwiseal-roofing.vercel.app). Paleta je uzeta iz Framer template-a Constra
(`ditsolution-constract.framer.website`).

## Šta je preuzeto, a šta promenjeno

**Preuzeto kako jeste:** cela anatomija komponenti i motion sistem iz `styles.css`
kiwiseal builda, plus `main.js` i `lenis.min.js`. Floating pill nav sa tri scroll
stanja, hero sa wash prelivom, podela naslova po rečima, scroll reveal, sticky
stacking kartice radova, subgrid kartice, overlapping process paneli, FAQ akordeon,
wizard forma i footer.

**Promenjeno na vaš zahtev:**

1. **Paleta je zamenjena Constra paletom**, tokeni su uzeti iz njihovog CSS-a:
   - `--ink` / `--deep` `#0B4654` (teal)
   - `--flame` `#FF6D45` (koral)
   - `--wash` `#F0F8FA`
   - `--muted` `#616161`
   - `--deep-2` `#15505E`, `--accent-light` `#3F646F`, hairline `rgba(140,140,140,.2)`
   Logo je narandžast `#ED7310`, što je blizu Constra korala, pa dobro stoji zajedno.
2. **Dugme se na hoveru ne pomera.** Uklonjen je `transform: translateY(-2px)` sa
   `.btn`, `.btn:active` i sa rotacije ikonice. Ostala je samo promena boje:
   koral prelazi u teal, ikonica iz bele u belu sa teal glifom. Isto je uklonjeno i
   sa `.choice` kartica u formi.
3. **Hero pill je urađen kao na Constri.** Izmereno sa njihovog sajta i preneto:
   pozadina `rgba(140,140,140,.2)`, radijus `999px`, padding `5px 10px 5px 5px`,
   gap `7px`, okrugla koral ikonica 20px, tekst 14px / 600 / uppercase, beo.
   Klasa je `.eyebrow` u heroju i `.eyebrow-ico` za ikonicu.
4. **Sticky kartice radova su veće.** Constra kartica je 1240x556 sa 50px paddinga,
   naša je sada 1310x520, slika 470x420, padding 45px, gap 50px. Ranije je bila
   padding 30px i slika 300x300.

## Mapa sekcija

| Sekcija kod nas | Blok iz reference |
|---|---|
| Hero | `.hero` |
| O nama + tri podatka | `.overview-top` + `.stat-row` |
| Za koga radimo (3 kartice) | `.feature-grid` |
| Proizvodi (foto + 5 redova) | `.services-split` |
| Naši radovi (3 sticky kartice) | `.project-stack` |
| Zašto Premium (2 kartice) | `.warranty-split` |
| Kako ide (3 koraka) | `.process-grid` |
| Unutrašnjost (2 kartice) | `.work-grid` |
| Česta pitanja | `.faq-split` |
| Još radova (2 kartice) | `.work-grid` |
| Footer | `.footer` |
| Wizard forma na kontaktu | `.wizard` |

**Sekcija recenzija (`.testi-grid`) namerno nije korišćena.** Klijent nema
objavljene recenzije, a lažne recenzije ne idu na sajt. Kada se otvori Google profil
i skupe prve ocene, blok postoji u `styles.css` i može da se ubaci bez novog CSS-a.

## Sadržaj

Copy je pisan na osnovu onoga što ljudi stvarno pitaju u komentarima na Instagramu:
cena, dimenzije, izrada po meri, koliko vozila staje u garažu, da li vrata ulaze u
cenu, kakva podloga treba. Ta pitanja su postala FAQ i koraci u formi, pa forma
unapred skuplja ono zbog čega se inače prepisuje u porukama.

**Cene nisu nigde objavljene**, u skladu sa dogovorom, dok ih klijent ne potvrdi.

## Slike

`images/` sadrži 16 fotografija sa Instagrama, preimenovanih u čitljiva imena
(`hero.jpg`, `garaza-antracit.jpg`, `terasa.jpg`, `enterijer-1.webp` i tako dalje) i
`logo.png`.

Dve grafike sa profila **nisu korišćene** jer imaju utisnut tekst preko slike
(reklama „Posebna ponuda 3850 EUR" i oglas „Tražimo radnike"). Fotografija sa
tekstom ispod naslova sekcije izgleda loše, pa su izostavljene. Dva videa takođe
nisu korišćena u ovom buildu.

## Šta još treba

1. **Backend forme.** `ENDPOINT` na vrhu `main.js` je prazan. Pokrenuti Skill 03.
2. **Imejl adresa** za primanje upita, trenutno je nema nigde na sajtu.
3. **Pravno ime firme, PIB i matični broj** za footer.
4. **Cene**, ili barem „od X EUR" po proizvodu, da se izbegne pitanje „cena?".
5. **Drugi broj telefona.** Na dve grafike sa profila stoji **063 697 110**, a u bio-u
   **061 743 6390**. Na sajtu je svuda 061 743 6390. Proveriti koji je glavni.
6. **Podatak o ceni sa grafike:** garaža je reklamirana kao 5.500 EUR sniženo na
   3.850 EUR. Nije stavljeno na sajt jer je akcijska cena, treba potvrda.
7. **WhatsApp ili Viber** broj za dugme na mobilnom, ako ga koriste.
8. **Google Business profil** za recenzije, pa da se uključi blok sa ocenama.

## Lokalni pregled

```bash
cd "C:/Users/pavle/Desktop/Premium Container Website" && python -m http.server 8321
```

Zatim otvoriti `http://127.0.0.1:8321/index.html`.
