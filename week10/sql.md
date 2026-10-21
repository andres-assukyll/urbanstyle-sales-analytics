SLAID 2: SQL JA ANDMETÖÖ (1 min 50 s)
Sõnum: kolmandik müügiridadest koosnes duplikaatidest, iga viies klient on ostmata, käive kasvas ligi 19%.

| Osa | Number | Täpsustus |
|---|---|---|
| 1. Lähtepunkt | 15 234 → 10 118 müügirida, 5116 duplikaati eemaldatud, Üle 4 mln € → 2,91 mln € | Kolmandik müügiridadest olid duplikaadid, eemaldasime need. ~1 500 müüki on ilma kliendita (käibes sees, klienditest väljas). Customers: e-postiprobleemid, tooted puhtad |
| 2. Ostuta kliendid | 599 klienti (19%) | Iga viies klient pole kunagi ostnud |
| 3. Käive | +19,1%, +235 599 €; jaanuar +7,4% | Käive kasvas ligi 19%, isegi nõrgimal kuul oli kasv. Piirang: ~10% käibest ei saa kliendiga siduda |
| 4. VIP-id | 19 VIP-i, 13,2% käibest; 14 neist Tallinnas/Pärnus | Paarkümmend klienti toob kaheksandiku käibest |
| 5. AI | - | SQL-päringute debugimine |
| 6. Üleminek | - | Sõna järgmisele |


KOLM NUMBRIT, MIS PEAVAD MEELDE JÄÄMA
| # | Number | Kõnes |
|---|---|---|
| 1 | 5 116 duplikaati | Kolmandik müügiridadest |
| 2 | 599 klienti | Iga viies on ostmata |
| 3 | +19,1% (+235 599 €) | Käive kasvas ligi 19% |

SLAIDI ÜLESEHITUS
- Pealkiri: järeldus
- Üleval: enne/pärast võrdlus (müügiread)
- All: kaks numbrikaarti (ostuta kliendid, käibekasv)
- VIP-id, (AI ja üleminek ainult kõnes, esitlusele ei pane)


TÄPSUSTUSED:
- Pärast 5 116 duplikaadi eemaldamist jäi alles 10 118 puhtat müügirida, millest umbes 1 500 on külalisostud (registreerimata kliendid)
- +19,1% on arvutatud tabelist, kus kliendita müügid on sees
