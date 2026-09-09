# Kliendigruppide analüüs – Week 4

**Tegija:** Andres Assuküll <br>
**Roll:** (B) Kliendigruppide analüüsija <br>
**Andmetabel:** `sales` ja `customers` <br><br> 

## 📋 LÜHIKOKKUVÕTE <br>
Segmenteerida kliendid kulutuse järgi **VIP** / **Regular** / **Uus**, leida `TOP kliendid` ja koostada kliendiprofiili kokkuvõte **Kristile**. <br>
> *Täielik analüüs on [leitav siit](https://github.com/andres-assukyll/daca-portfolio/blob/main/week-4/README.md)*.

---

## TULEMUSED

### Käive

![Käive](https://github.com/andres-assukyll/daca-portfolio/blob/main/week-4/img/kaibe-vordlus.svg)

### Kliendisegmendid

![Kliendisegmendid](https://github.com/andres-assukyll/daca-portfolio/blob/main/week-4/img/segmentide-tabel.svg)


### Asukohad
![Asukohad](https://github.com/andres-assukyll/daca-portfolio/blob/main/week-4/img/vip-kliendid-linnade-kaupa.svg)

#### Lisaks
Kõik VIP kliendid on sooritanud oste kõigist UrbanStyle.ltd müügikohtadest ning rohkem kulutanud kas Tallinna poes või veebipoes.

[Analüüsis kastutatud SQL koodid](https://github.com/andres-assukyll/daca-portfolio/blob/main/week-4/week4_customer_segmentation_aggregation.sql)

---

#### JÄRELDUS
Tuvastatud klientide käive moodustab **90% kogukäibest**. Kõige väärtuslikumasse segmenti kuulub vaid **19 VIP-klienti**, kelle käive moodustab **13,2% kogukäibest** ja kellest **14** asuvad Tallinnas või Pärnus.

**Tugev tulemus**: üks VIP teeb keskmiselt umbes 20 korda rohkem käivet kui teiste segmentide kliendid.
- **19** VIP klienti moodustavad vaid **0.74%** kogu kliendibaasist **2 551**. <br>
- Nad annavad **13.2%** kogukäibest. <br>
- Ühe VIP kliendi keskmine käive on **18 227 €**. <br>
- Ülejäänud klientide keskmine käive on ligikaudu **900 €**. 

**Koondumisrisk**: VIP-i lahkumine võib oluliselt mõjutada kogukäivet. <br>
> *Seega tasub VIP-e hoolega hoida ning samal ajal üritada kasvatada teistest klientidest uusi VIP-e*.

---

## SUURIM ÜLLATUS                                       

VIP kliendi keskmine käive on **18 227 €**, mis on **11.3** korda suurem kui tavaklientidel ja **37** korda suurem kui uutel klientidel.                                       

## SOOVITUS KRISTILE                                        

Hoia fookus `VIP` klientide säilitamisel ning `tavaklientide` kasvatamisel VIP tasemele, eelkõige Tallinnas ja Pärnus.

## PUUDUVAD ANDMED

Pole.

