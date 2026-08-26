# Sales data cleaner -Week 2

**Tegija:** Evelyn Uusmaa
**Roll:* Sales data cleaner
**Andmetabel:* 'sales'

## 📌 Kokkuvõte

| Kategooria | Leitud probleeme | Tehtud muudatus | 
|---|---|---:|
| Duplikaadid | 5116 | Üleliigsed kordused eemaldati |
| NULL customer_id | 1487 | Probleemsed read eemaldati |
| NULL sale_date | 0 | Probleemsed read eemaldati |
| NULL total_price | 0 | Probleemsed read eemaldati |
| Tuleviku kuupäevad | 0 |Probleemsed read eemaldati |


## 💡 Järeldused

Andmestikku jäi järgi 9314 rida. 
Korrigeeritud andmetest eemaldati duplikaadid, puuduva kliendita read, sest müüki ei saa kliendiga seostada, puuduva kuupäevaga read, sest müüki ei saa ajaliselt analüüsida,
puuduva summaga read, sest neid ei saa müügituli arvutamisel kasutada, tuleviku kuupäevaga read.
