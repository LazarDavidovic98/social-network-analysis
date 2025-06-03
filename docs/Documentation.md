# Projekat: Analiza socijalne mreže naučne kolaboracije

Ova dokumentacija pokriva sve tehničke i analitičke aspekte projekta koji je realizovan u okviru predmeta *Analiza socijalnih mreža*. Fokus projekta je analiza naučne kolaboracije zaposlenih na Medicinskom fakultetu Univerziteta u Beogradu, korišćenjem metoda iz oblasti mrežne analize.

---

## Dataset

**Korišćeni fajlovi:**
- `autori.xlsx` – lista relevantnih autora (zaposlenih na katedrama)
- `epidemiologija.xlsx`, `imunologija.xlsx`, `infektivne_bolesti.xlsx`, `mikrobiologija.xlsx` – sirovi podaci o publikacijama, koje treba srediti
- `mreza_casopisa.gml` – graf mreže časopisa

**Kolone u .xlsx fajlovima:**
- `Author`, `Authors`, `Title`, `Year`, `Source title`, `Volume`, `Issue`, `Art. No.`, `Page start`, `Page end`, `Page count`, `Cited by`, `Link`, `Document Type`, `Source`

**Filtriranje:**
- Uključeni samo radovi tipa: Article, Article in Press, Review, Book Chapter, Letter, Note
- Samo autori iz fajla `autori.xlsx`

---

## Korišćene biblioteke i alati

- `pandas` – obrada tabela
- `networkX` – kreiranje i analiza mreža
- `matplotlib`, `graphviz` – vizualizacija
- `Gephi` – napredna vizuelna analiza i Louvain detekcija komuna

---

## 🧮 Ključne analize

### Statistička analiza
- Broj radova po autoru (celovito i frakciono)
- Prosečan broj koautora
- Izračunavanje H-indeksa po autoru i poređenje sa datim vrednostima
- Analiza produktivnosti po godinama i katedrama
- Frekvencija publikacija po časopisima

### Modelovanje mreže
- Građenje neusmerene težinske mreže koautora
- Građenje mreže časopisa iz fajla `mreza_casopisa.gml`

### Mrežne metrike
- Gustina mreže
- Dijametar i prosečna udaljenost
- Koeficijenti klasterizacije (globalni, lokalni)
- Asortativnost po stepenu
- Rich-club analiza (poređenje sa Havel-Hakimi grafom)
- Power-law distribucija stepena čvorova

### Centralnost
- Stepen, bliskost, betweenness, sopstveni vektor
- Izrada kompozitne centralnosti (heuristika)
- Identifikacija ključnih autora i brokera među katedrama

### Detekcija komuna
- **Louvain metoda** (Gephi) – vizualizacija i analiza uticaja rezolucije
- **Spektralno klasterisanje** – uz poređenje sa Girvan-Newman algoritmom
- Analiza smislenosti komuna i identifikacija mostova među grupama

---

## Zaključci i preporuke

- Identifikovani ključni akteri mreže mogu biti kandidati za dalje povezivanje naučnih timova
- Mreža pokazuje karakteristike malog sveta i asortativnosti
- Kompozitna centralnost pomaže u rangiranju autora sa najznačajnijim uticajem

---

## Tehnički detalji

- Projekat pisan u Python-u 3.9
- .ipynb fajlovi izvršavani u Jupyter Notebook okruženju
- Vizuelizacije mreža izvođene delimično u Gephi i delimično u Python-u
- Upotrebljeni grafovi su neusmereni i težinski (broj zajedničkih radova)

---

<p style="color:#999999;">© 2024 Lazar Davidović — Elektrotehnički fakultet, Univerzitet u Beogradu<br/>
© 2024 Luka Simić — Elektrotehnički fakultet, Univerzitet u Beogradu</p>