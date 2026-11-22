# ETL projekat – Da li pobede prodaju dresove?

## Opis projekta

Cilj projekta je analiza prodaje sportske opreme za 20 klubova NSL lige i utvrđivanje da li rezultati utakmica utiču na prodaju proizvoda.

## Izvori podataka

Podaci se preuzimaju iz četiri izvora:
- Porudžbine – API (JSON).
- Proizvodi – CSV fajl.
- Timovi – CSV fajl.
- Utakmice – Parquet fajl.

## Obrada podataka

Pipeline se sastoji iz tri glavna koraka:

1. **Extract** – preuzimanje podataka iz svih izvora i čuvanje sirovih podataka.
2. **Transform** – čišćenje podataka, uklanjanje duplikata, validacija porudžbina i analiza rezultata utakmica.
3. **Load** – čuvanje obrađenih podataka u CSV i Parquet fajlovima.

## Rezultati analize

- Ukupan broj porudžbina: 1852.
- Broj ispravnih porudžbина: 1800.
- Broj odbačenih porudžbina: 52.
- Broj duplikata: 12.
- Najveći promet po timu ostvario je LSB sa 720.420 RSD.
- Najprodavanija kategorija su dresови (jerseys), sa prometom od 7.094.410 RSD.

Prosečan dnevni promet nakon pobede iznosi 8.847,29 RSD, dok nakon poraza iznosi 2.986,22 RSD.

## Zaključak

Rezultati analize pokazuju da postoji povezanost između uspeha timova i prodaje sportske opreme. Prodaja je veća nakon pobeda, a manja nakon poraza.

## Korišćene tehnologije

Python, Pandas, Requests, JSON, CSV, Parquet i Jupyter Notebook.
