# Excel Election Seat Allocation

Excel-pohjainen vaalien paikkajaon analyysiprojekti, jossa käytetään ehdokkaiden äänidataa, lajittelua, vertailulukuja ja tulosten järjestämistä.

## Projektin tarkoitus

Tämä projekti tutkii, miten vaalituloksia voidaan laskea taulukkolaskennan menetelmillä. Pääpaino on datan siistimisessä, ryhmittelyssä, vertailulukujen muodostamisessa, järjestämisessä ja paikkajaon osoittamisessa.

Projekti on tarkoituksella menetelmäkeskeinen. Lähdedokumentteja käytetään oppimis- ja vertailumateriaalina, mutta repository esittää laskentamenetelmän itsenäisenä data-analyysiprojektina.

## Lähdeaineisto

Laskenta perustuu opettajan antamaan Excel-tiedostoon ja tuloksia tarkistetaan julkista virallista vaalitulosaineistoa vasten.

Virallinen vertailuaineisto:

- Oikeusministeriön vaalien tulospalvelu / Eduskuntavaalit 2023
- Pirkanmaan vaalipiirin ehdokaskohtaiset tulokset
- Tarkastuslaskenta valmis

## Tiedostot

| Tiedosto | Kuvaus |
|---|---|
| [`index.html`](index.html) | Interaktiivinen tulosten tarkastelusivu |
| [`data/raw/candidate-votes.csv`](data/raw/candidate-votes.csv) | Siistitty ehdokasäänidata |
| [`data/processed/dhondt-results.csv`](data/processed/dhondt-results.csv) | Lasketut 20 valittua ehdokasta D’Hondt-vertailuluvulla |
| [`data/processed/party-seat-summary.csv`](data/processed/party-seat-summary.csv) | Puolueiden äänimäärät ja lasketut paikat |
| [`docs/validation-notes.md`](docs/validation-notes.md) | Validointihuomiot ja laskentalogiikan tarkistus |

## Laskentamenetelmä

Korjattu laskenta käyttää D’Hondt-tyyppisiä vertailulukuja:

1. Lasketaan puolueen/listan kokonaisäänet.
2. Järjestetään puolueen ehdokkaat henkilökohtaisten äänten perusteella.
3. Annetaan jokaiselle ehdokkaalle puolueensisäinen sijoitus.
4. Lasketaan vertailuluku:

```text
vertailuluku = puolueen kokonaisäänet / ehdokkaan puolueensisäinen sijoitus
```

5. Kaikki ehdokkaat järjestetään vertailuluvun mukaan.
6. Valitaan 20 suurinta vertailulukua.

## Laskettu paikkajako

| Puolue | Äänet | Paikat |
|---|---:|---:|
| SDP | 80131 | 6 |
| KOK | 66545 | 5 |
| PS | 62496 | 5 |
| VIHR | 23241 | 1 |
| KESK | 22010 | 1 |
| VAS | 21307 | 1 |
| KD | 16912 | 1 |

## Mitä projekti osoittaa

- Excel-/taulukkolaskentalogiikka
- datan siistiminen ja järjestely
- puoluekohtaisten kokonaisäänien laskenta
- D’Hondt-vertailulukujen muodostaminen
- tulosten validointi virallista lähdettä vasten
- interaktiivinen HTML-tulosten tarkastelu

## Lisenssi

MIT License
