# roilasku

Satafarma & Greige ROI — apteekin oman työntekijän ja ulkoistetun työn
kustannusvertailu sekä neljän vuoden säästölaskelma. Itsenäinen PWA: ei
backendiä, ei riippuvuuksia, toimii offline.

## Sisältö

- `index.html` — koko sovellus (HTML, CSS, JS, SVG-kaavio yhdessä tiedostossa)
- `manifest.json` — PWA-manifesti (nimi, värit, ikonit)
- `sw.js` — service worker, joka tallentaa sovelluksen offline-käyttöön
- `icon-192.png`, `icon-512.png`, `icon-maskable-512.png` — ikonit

## Julkaisu GitHub Pagesilla

1. Luo repo nimellä `roilasku` ja työnnä nämä tiedostot juureen.
2. Settings → Pages → Source: `Deploy from a branch`, branch `main`, kansio `/ (root)`.
3. Osoite tulee muotoon `https://<käyttäjä>.github.io/roilasku/`.

Service worker ja manifest käyttävät suhteellisia polkuja, joten ne toimivat
suoraan myös alikansiopolusta (`/roilasku/`).

## Vaihtoehto ilman Gitiä

Raahaa tämä kansio osoitteeseen <https://app.netlify.com/drop> — saat heti
https-linkin, jonka voi jakaa ja asentaa.

## Asennus puhelimeen

Avaa osoite Safarissa (iOS) tai Chromessa (Android) → Jaa → *Lisää
kotinäyttöön*. Sovellus avautuu omasta kuvakkeestaan kokoruututilassa.

## Päivittäminen

Kun muutat `index.html`-tiedostoa, nosta `sw.js`:ssä cache-versiota
(`roilasku-v1` → `roilasku-v2`). Näin vanha välimuisti siivotaan ja käyttäjät
saavat uuden version.

## Laskennan oletukset

- Vuoron pituus 8 h ja 52 työviikkoa vuodessa (säädettävissä kohdassa *Oletukset*).
- Työntekijän palkka maksetaan koko vuodelta; ulkoistettua työtä ja lisämyyntiä
  lasketaan vain todellisilta työviikoilta (52 − loma).
- Ulkoistetun vuoroja/viikko (oletus 4,0) ja työviikkojen määrä on johdettu
  alkuperäisen laskurin luvuista; tarkista ja säädä tarvittaessa.

Oletusarvoilla neljän vuoden säästö on −80 628 € (ulkoistus kalliimpi).
