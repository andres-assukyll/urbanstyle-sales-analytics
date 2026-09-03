# Customers Without Purchases – Week 3

**Tegija:** Evelyn Uusmaa  
**Roll:** Customers Without Purchases  
**Kasutatud tabelid:** `customers`, `sales`

## Ülesanne

Minu ülesanne oli ühendada `customers` ja `sales` tabelid ning leida registreerunud kliendid, kes pole teinud ühtegi ostu. Lisaks analüüsisin nende asukohta ja registreerumise aega ning koostasin tulemuste põhjal soovituse turundusjuhile Anna Metsale.

## Peamised tulemused

| Näitaja | Tulemus |
| --- | ---: |
| Kliente kokku | 3150 |
| Aktiivseid kliente | 2551 |
| Ostuta kliente | 599 |
| Ostuta klientide osakaal | 19% |

Kõige rohkem ostuta kliente oli Tallinnas (221), Tartus (133) ja Pärnus (70).

## Kasutatud meetod

Ostuta klientide leidmiseks kasutasin `LEFT JOIN` ühendust ning kontrollisin, millistel klientidel puudus vastav müügikirje.

```sql
SELECT COUNT(*) AS kadunud_kliente
FROM customers AS c
LEFT JOIN sales AS s
    ON c.customer_id = s.customer_id
WHERE s.sale_id IS NULL;
```

## Peamine leid

Ligi viiendik UrbanStyle’i registreerunud klientidest pole pärast registreerumist teinud ühtegi ostu. Suurim kasutamata potentsiaal asub Tallinnas ja Tartus.

## Soovitus Annale

UrbanStyle’i kliendibaasis on 599 registreerunud klienti, kes pole veel ühtegi ostu teinud. Esimese kampaania võiks suunata Tallinna ja Tartu ostuta klientidele, sest neis linnades on neid kõige rohkem. Hiljuti liitunud ja pikemat aega passiivsetele klientidele võiks saata erineva sõnumiga pakkumised. Esimese ostu soodustus või ajaliselt piiratud personaalne pakkumine võiks aidata muuta need kontaktid aktiivseteks klientideks.

## Minu panus

- ühendasin `customers` ja `sales` tabelid;
- leidsin ostuta kliendid;
- arvutasin aktiivsete ja ostuta klientide arvu;
- analüüsisin tulemusi linnade ja registreerumisaja järgi;
- koostasin turundusjuhile praktilise soovituse.

## Põhjalik analüüs

- [SQL JOIN-id ja kadunud klientide analüüs minu portfoolios](https://github.com/Nordmehr/daca-portfolio/blob/main/week-3/README.md)