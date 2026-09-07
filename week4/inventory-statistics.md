# Inventory Statistics – Week 4

**Tegija:** Evelyn Uusmaa  
**Roll:** Inventory Statistics  
**Kasutatud tabelid:** `products`, `sales`, `inventory_movements`

## Ülesanne

Minu ülesanne oli analüüsida tootekategooriaid, toodete hindu ja müügikoguseid. Kasutasin `GROUP BY`, `HAVING` ja window function’e, et võrrelda kategooriaid ning järjestada tooted kategooriate sees. Lisaks leidsin iga kategooria kolm enim müüdud toodet ja koostasin tulemuste põhjal soovitused turundusjuhile Anna Metsale.

## Peamised tulemused

| Näitaja | Tulemus |
|---|---:|
| Analüüsitud kategooriaid | 5 |
| Kõige rohkem tooteid | meeste riided – 82 |
| Kõige suurem müügikogus | meeste riided – 4121 |
| Kõrgeim keskmine jaehind | jalanõud – 214,10 € |
| Suurim keskmine müük toote kohta | laste riided – 64,33 |

Kõige rohkem erinevaid tooteid ja suurim müügikogus oli meeste riiete kategoorias. Laste riiete kategoorias oli kõige suurem keskmine müüdud kogus ühe müüdud toote kohta.

## Kasutatud meetod

Kategooriate analüüsimiseks ühendasin `products` ja `sales` tabelid veeru `product_id` kaudu. Kasutasin `GROUP BY` käsku kategooriate moodustamiseks ning `HAVING` tingimust grupeeritud müügitulemuste filtreerimiseks.

```sql
SELECT
    p.category,
    COUNT(DISTINCT p.product_id) AS myydud_tooteid,
    SUM(s.quantity) AS myydud_kogus,
    ROUND(
        SUM(s.quantity)::numeric
        / COUNT(DISTINCT p.product_id),
        2
    ) AS keskmine_kogus_toote_kohta
FROM products p
JOIN sales s
    ON p.product_id = s.product_id
GROUP BY p.category
HAVING SUM(s.quantity) > 100
ORDER BY myydud_kogus DESC;
```

Toodete järjestamiseks kategooria sees kasutasin `ROW_NUMBER()` window function’it koos `PARTITION BY` käsuga.

## Peamine leid

Meeste riided olid müügikoguse järgi kõige tugevam kategooria. Laste riiete kategoorias oli väiksem tootevalik, kuid kõige suurem keskmine müük ühe müüdud toote kohta. Jalanõudel oli analüüsitud kategooriatest kõige kõrgem keskmine jaehind.

## Soovitus Annale

Meeste riiete tugevat müüki tasub toetada piisava laovaru ja nähtavusega kampaaniates. Laste riiete populaarsemate toodete laoseisu tuleks kontrollida, sest nende keskmine müük toote kohta oli kõige kõrgem. Aksessuaaride müügi suurendamiseks võiks katsetada komplektipakkumisi koos riiete või jalanõudega. Tegeliku kasumlikkuse hindamiseks tuleks järgmises analüüsis võrrelda müügitulu ka toodete omahinna ja laoseisuga.

## Minu panus

- koostasin tootekategooriate koondanalüüsi;
- arvutasin kategooriate müüdud kogused;
- kasutasin tulemuste filtreerimiseks `HAVING` tingimust;
- järjestasin tooted kategooriate sees window function’iga;
- leidsin iga kategooria TOP 3 tooted;
- koostasin tulemuste põhjal ärilised soovitused.

## Põhjalik analüüs

- [Inventuuristatistika ja kategooriate müügianalüüs minu portfoolios](https://github.com/Nordmehr/daca-portfolio/blob/main/week-4/README.md)