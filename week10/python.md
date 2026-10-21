
# SLAID 4: PYTHON – ANDMEANALÜÜSIST AUTOMATISEERIMISENI

**Esitaja:** Andres Assuküll  
**Kestus:** kuni 2 minutit  
**Alus:** nädalate 7 ja 8 kogu tiimitöö

## Põhisõnum

Python aitas meil liikuda ühekordsest andmeanalüüsist
korratava, kontrollitava ja automatiseeritud aruandluseni.

## Esitluse ülesehitus

| Osa | Aeg | Põhinumber või tegevus |
|---|---|---|
| 1. Pandas ja RFM | ~30 s | 2540 klienti, 5 segmenti |
| 2. Pipeline | ~45 s | API → Pandas → Plotly → eksport |
| 3. Veakäsitlus | ~20 s | 3 korduskatset, SUCCESS/WARNING/FAILURE |
| 4. Äriline väärtus | ~20 s | 55–100 min → 2–5 min |

## 1. Nädal 7 – Pandas ja RFM

- Müügi- ja kliendiandmete laadimine ning ühendamine.
- Andmete puhastamine ja ettevalmistamine.
- RFM-analüüs: 2540 ostnud klienti, 5 segmenti.
- Potential: 768 klienti (30,2%).
- At Risk: 524 klienti (20,6%).
- Plotly visualiseeringute asemel kasutati nädal 7
  dokumentatsioonis kliendisegmentide graafikuid.
- Soovitused kliendisegmentide aktiveerimiseks,
  hoidmiseks ja tagasivõitmiseks.

## 2. Nädal 8 – automatiseeritud pipeline

**Töövoog:**

Supabase API → Pandas → Plotly → CSV/HTML → e-post

- API päringud ja andmete laadimine 1000 rea kaupa.
- Andmete valideerimine, puhastamine ja KPI-de arvutamine.
- Nädalase müügitulu graafik ja KPI-tabel.
- CSV- ja HTML-väljundid.
- Mitme perioodi töötlemine ühe käivitusega.
- Üks koondteavitus kogu jooksu kohta.

## 3. Veakäsitlus

- Ühendusvea korral 3 korduskatset.
- Katsete vahel 30 sekundit.
- SUCCESS – kõik perioodid õnnestusid.
- WARNING – osa perioode ebaõnnestus.
- FAILURE – kõik perioodid ebaõnnestusid.
- Vigaste andmetega ei jätkata.
- Asendusandmeallikat praegu ei ole.

## 4. Äriline väärtus

| Käsitsi | Automatiseeritult |
|---|---|
| 55–100 min | 2–5 min |

*Ajad on projekti dokumentatsioonis esitatud hinnangud.*

## Kolm asja, mis peavad meelde jääma

1. **2540 klienti** – RFM-analüüs ja 5 segmenti.
2. **Üks pipeline** – andmete laadimisest teavituseni.
3. **2–5 minutit** – hinnanguline automatiseeritud tööaeg.

## Seos SQL-esitlusega

SQL: mida andmed meile näitasid?  
Python: kuidas analüüsi korrata ja automatiseerida?

Vältida SQL-osa numbrite kordamist.

## Slaidi interaktiivsus

- Klõpsatavad pipeline'i etapid.
- Iga etapi juures selgitus ja koodinäide.
- SUCCESS/WARNING/FAILURE simulatsioon.
- Püsiv ajavõidu võrdlus.

## Lõpusõnum

**Python muutis analüüsi korratavaks, kontrollitavaks
ja juhtimisotsuste jaoks kiiremini kasutatavaks.**
