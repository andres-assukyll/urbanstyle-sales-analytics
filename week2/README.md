## MEESKOND: Sales Analytics  |  NÄDAL: 2 |  TEGELANE: Toomas Kask

   ### Meeskonnaliikmed
   | Nimi | Roll (Nädal 2) | OS |
   |---|---|:---:|
   | [Evelyn Uusmaa](sales-data-cleaner.md) | A: Sales Data Cleaner | Win |
   | [Nele Kund](customer-data-cleaner.md) | B: Customer Data Cleaner | Win |
   | [Andres Assuküll](product-data-cleaner.md) | C: Product Data Cleaner | Mac |

---

## Andmekvaliteedi koondraport

```text
PEAMISED LEIUD:
1. Sales: leitud 6603 ebaptäsete andmetega müügirida, mis eemaldati.
2. Customers: leitud 520 kliendiandmetega seotud probleemi.
3. Products: 12 duplikaatset toodet, mis eemaldati.


SUURIM ÜLLATUS:
Müügiandmetes leidus 5116 üleliigset duplikaatrida.
korduvaid invoice_id väärtused esinesid tabelis 1487 korda.
Tooteandmed olid üpris puhtad.
Kliendiandmete tabelis oli iga unikaalse linna kohta vähemalt 2 erinevat nimekuju.

SOOVITUS TOOMASELE:
Esimesena tuleks parandada duplikaatide tekkimise põhjus, sest korduvad
müügiread võivad näidata tegelikust suuremat müügitulu ja tellimuste arvu.
Edaspidi võiks invoice_id kordumist kontrollida juba andmete sisestamisel.

Kliendiandmete puhul selgitada esmalt välja puuduvate e-mailide põhjused ja võimalusel täiendada kontaktandmeid, sest need mõjutavad tellimuste kinnituste saatmist, klientide teavitamist ja turunduskampaaniate efektiivsust.

PUUDUVAD ANDMED:
Puuduvate customer_id väärtuste tõttu ei saa kõiki oste kliendiga siduda.
Puuduvate sale_date ja total_price väärtustega müüke ei saa täielikult
kasutada müügi- ega perioodianalüüsis.
Pole teada, kas puuduvaid meiliaadresse saab olemasolevate andmete põhjal tuletada või on vaja kliendi sisendit.
```
