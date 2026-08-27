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
MEESKOND: Operatsioonid  |  NÄDAL: 2  |  TEGELANE: Toomas Kask

ROLL: Müügiandmete puhastaja (Sales Data Cleaner)

PEAMISED LEIUD:
1. Sales: leitud 6603 ebaptäsete andmetega müügirida, mis eemaldati.
2. Customers: leitud 520 kliendiandmetega seotud probleemi.
3. Products: 12 duplikaatset toodet, mis eemaldati.


SUURIM ÜLLATUS:
Müügiandmetes leidus 5116 üleliigset duplikaatrida.
korduvaid invoice_id väärtused esinesid tabelis 1487 korda.
Tooteandmed olid üpris puhtad.

SOOVITUS TOOMASELE:
Esimesena tuleks parandada duplikaatide tekkimise põhjus, sest korduvad
müügiread võivad näidata tegelikust suuremat müügitulu ja tellimuste arvu.
Edaspidi võiks invoice_id kordumist kontrollida juba andmete sisestamisel.

PUUDUVAD ANDMED:
Puuduvate customer_id väärtuste tõttu ei saa kõiki oste kliendiga siduda.
Puuduvate sale_date ja total_price väärtustega müüke ei saa täielikult
kasutada müügi- ega perioodianalüüsis.
```
