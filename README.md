# 📊 Socijalna Mreža Naučne Kolaboracije - Medicinski Fakultet UB

Ovaj projekat predstavlja sveobuhvatnu analizu naučne produkcije i kolaboracije među zaposlenima na četiri katedre Medicinskog fakulteta Univerziteta u Beogradu: **Imunologija, Epidemiologija, Infektivne bolesti i Mikrobiologija**. Projekat je realizovan u okviru predmeta *Analiza socijalnih mreža* na Elektrotehničkom fakultetu u Beogradu.

Cilj analize je modelovanje i analiza **mreža koautora** i **mreža naučnih časopisa** kroz metrike mrežnog grafa, centralnosti, detekciju komuna i vizualizaciju, koristeći realne podatke prikupljene iz **Scopus baze** i fakultetskih izvora.

## Opis projekta

Projekat uključuje sledeće korake:
- Prečišćavanje i spajanje sirovih podataka iz više Excel fajlova (`epidemiologija.xlsx`, `imunologija.xlsx`, itd.)
- Filtriranje autora na osnovu liste zvaničnih zaposlenih (`autori.xlsx`)
- Konstrukcija grafa koautora i grafa časopisa pomoću `NetworkX`
- Analiza centralnosti (stepen, bliskost, sopstveni vektor, betweenness)
- Detekcija komuna (Louvain metod, spektralno klasterisanje)
- Upoređivanje sa slučajnim mrežama i merenje karakteristika kao što su gustina, klasterizacija, asortativnost, itd.
- Vizuelizacija mreža i interpretacija rezultata

## Korišćene tehnologije

- `Python` (v3.9+)
- `pandas` – za rad sa tabelama
- `networkX` – za modelovanje i analizu mreža
- `matplotlib` / `graphviz` – za vizuelizaciju
- `Gephi` – za naprednu vizuelnu analizu i Louvain detekciju komuna

## Ključne analize

- Broj radova po autoru (celovito i frakciono brojanje)
- H-indeks autora
- Distribucija po godinama i časopisima
- Mrežne metrike: klasterizacija, centralnost, asortativnost, dijametar
- Detekcija ključnih pojedinaca i komuna u naučnoj mreži

## Cilj

Pomoću alata iz oblasti analize socijalnih mreža, identifikovati:
- najvažnije naučne aktere,
- nivo kolaboracije među autorima i između katedri,
- strukturalne obrasce naučne produkcije,
- potencijalne preporuke za povezivanje izolovanih grupa ili autora.

---
**Detaljna dokumentacija dostupna je ovde**: [Documentation](docs/Documentation.md)

**Mozete pogledati i prezentaciju projekta**: [Presentation](docs/Presentation.pdf)
