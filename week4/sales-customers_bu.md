# Kliendigruppide analüüs – Week 4

**Tegija:** Andres Assuküll <br>
**Roll:** (B) Kliendigruppide analüüsija <br>
**Andmetabel:** `sales` ja `customers` <br><br> 

## 📋 LÜHIKOKKUVÕTE <br>
Segmenteerida kliendid kulutuse järgi (VIP / Regular / Uus), leida TOP kliendid ja koostada kliendiprofiili kokkuvõte Annale. <br>
> *Täielik analüüs on [leitav siit](https://github.com/andres-assukyll/daca-portfolio/blob/main/week-4/README.md)*.

---

## Tulemused

### Käive

| Kogukäive  | Klientide kogukäive | Klientide keskmine käive |Keskmine käive |
| :--------: | :-----------------: | :-----------------: |:---: |
| 2 909 177.98 EUR | 2 622 731.78 EUR | 1 028.12 EUR | 1 139.96 EUR |


### Kliendisegmendid
VIP piir > 5 000 € : kokku 19 klienti <br>
Regular piir > 1 000 € : kokku 917 klienti <br>
Uus piir < 1 000 € : kokku 1 615 klienti 

| Segment | Klientide arv | Keskmine käive |
| ------- | ------------: | -------------: |
| VIP     | 19            | 18 227.01 EUR  |
| Regular | 917           | 1 615.43 EUR   |
| Uus     | 1 615         | 492.30 EUR     |


#### VIP klientide asukohad

| Linn     | VIP klientide arv |
| -------- | :---------------: |
| Tallinn  | 8                 |
| Pärnu    | 6                 |
| Tartu    | 2                 |
| Jõhvi    | 1                 |
| Rakvere  | 1                 |
| Viljandi | 1                 |

Kõik VIP kliendid on oste sooritanud kõigist UrbanStyle.ltd müügikohtadest ning rohkem kulutanud kas Tallinna poes või veebipoes.

---

#### Top 10 VIP klienti müügikohtade kaupa

| Nimi         | Linn     | Müügikoht   | Müügikoha kogukäive | Tellimusi müügikohas | Kliendi kogukäive |
| ------------ | -------- | --------- | ----------------: | ---------------------: | ----------------: |
| Tiina Pärn   | Tartu    | veebimüük | 14 679 EUR        | 24                     | 27 668 EUR        |
| Tiina Pärn   | Tartu    | Tallinn   | 6 825 EUR         | 28                     | 27 668 EUR        |
| Tiina Pärn   | Tartu    | Tartu     | 4 150 EUR         | 16                     | 27 668 EUR        |
| Tiina Pärn   | Tartu    | Pärnu     | 2 014 EUR         | 5                      | 27 668 EUR        |
| Priit Rand   | Pärnu    | Tallinn   | 9 602 EUR         | 24                     | 26 286 EUR        |
| Priit Rand   | Pärnu    | veebimüük | 8 694 EUR         | 33                     | 26 286 EUR        |
| Priit Rand   | Pärnu    | Tartu     | 6 381 EUR         | 14                     | 26 286 EUR        |
| Priit Rand   | Pärnu    | Pärnu     | 1 608 EUR         | 5                      | 26 286 EUR        |
| Kevin Org    | Tallinn  | veebimüük | 8 408 EUR         | 25                     | 23 467 EUR        |
| Kevin Org    | Tallinn  | Tallinn   | 8 247 EUR         | 26                     | 23 467 EUR        |
| Kevin Org    | Tallinn  | Tartu     | 5 323 EUR         | 19                     | 23 467 EUR        |
| Kevin Org    | Tallinn  | Pärnu     | 1 489 EUR         | 8                      | 23 467 EUR        |
| Laura Tammik | Pärnu    | Tallinn   | 8 244 EUR         | 31                     | 23 386 EUR        |
| Laura Tammik | Pärnu    | Tartu     | 5 380 EUR         | 15                     | 23 386 EUR        |
| Laura Tammik | Pärnu    | veebimüük | 5 095 EUR         | 17                     | 23 386 EUR        |
| Laura Tammik | Pärnu    | Pärnu     | 4 667 EUR         | 11                     | 23 386 EUR        |
| Erkki Ilves  | Tartu    | veebimüük | 8 376 EUR         | 29                     | 22 942 EUR        |
| Erkki Ilves  | Tartu    | Tallinn   | 8 024 EUR         | 23                     | 22 942 EUR        |
| Erkki Ilves  | Tartu    | Tartu     | 4 209 EUR         | 14                     | 22 942 EUR        |
| Erkki Ilves  | Tartu    | Pärnu     | 2 332 EUR         | 6                      | 22 942 EUR        |
| Anu Kuusik   | Tallinn  | Tallinn   | 11 312 EUR        | 34                     | 21 626 EUR        |
| Anu Kuusik   | Tallinn  | veebimüük | 5 827 EUR         | 21                     | 21 626 EUR        |
| Anu Kuusik   | Tallinn  | Tartu     | 3 355 EUR         | 14                     | 21 626 EUR        |
| Anu Kuusik   | Tallinn  | Pärnu     | 1 132 EUR         | 8                      | 21 626 EUR        |
| Kersti Lill  | Tallinn  | Tallinn   | 11 130 EUR        | 41                     | 21 137 EUR        |
| Kersti Lill  | Tallinn  | veebimüük | 5 014 EUR         | 12                     | 21 137 EUR        |
| Kersti Lill  | Tallinn  | Pärnu     | 2 728 EUR         | 11                     | 21 137 EUR        |
| Kersti Lill  | Tallinn  | Tartu     | 2 266 EUR         | 7                      | 21 137 EUR        |
| Riina Lill   | Pärnu    | veebimüük | 10 073 EUR        | 28                     | 20 972 EUR        |
| Riina Lill   | Pärnu    | Tallinn   | 6 816 EUR         | 25                     | 20 972 EUR        |
| Riina Lill   | Pärnu    | Tartu     | 3 756 EUR         | 10                     | 20 972 EUR        |
| Riina Lill   | Pärnu    | Pärnu     | 327 EUR           | 4                      | 20 972 EUR        |
| Annika Saar  | Viljandi | Tallinn   | 8 543 EUR         | 21                     | 20 727 EUR        |
| Annika Saar  | Viljandi | veebimüük | 8 339 EUR         | 31                     | 20 727 EUR        |
| Annika Saar  | Viljandi | Pärnu     | 2 142 EUR         | 5                      | 20 727 EUR        |
| Annika Saar  | Viljandi | Tartu     | 1 702 EUR         | 9                      | 20 727 EUR        |
| Ago Kull     | Pärnu    | veebimüük | 10 008 EUR        | 28                     | 20 125 EUR        |
| Ago Kull     | Pärnu    | Tallinn   | 6 965 EUR         | 23                     | 20 125 EUR        |
| Ago Kull     | Pärnu    | Pärnu     | 2 175 EUR         | 8                      | 20 125 EUR        |
| Ago Kull     | Pärnu    | Tartu     | 977 EUR           | 5                      | 20 125 EUR        |

