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

## Peamine leid

Kõige suurem müügikoormus langeb meeste riiete kategooriale, millest müüdi kokku 4121 ühikut. Laste riiete kategoorias oli aga kõige suurem keskmine müük ühe toote kohta – 64,33 ühikut –, mis võib tähendada, et nõudlus koondub väiksemale arvule toodetele. Need kategooriad vajavad varude planeerimisel esmajärjekorras tähelepanu, sest ebapiisav laoseis võib seal kõige kiiremini müügikadu põhjustada.

## Soovitus Liisile /Liisile? Kas mitte Annale?/

Kontrolli esmajärjekorras Tartu poe meeste ja laste riiete laoseisu, sest nende kategooriate müügimaht on kõige suurem ning puudulik laovaru võib kiiresti müügikadu põhjustada. Võrdle süsteemis näidatud koguseid tegeliku inventuuri ning `IN`, `OUT`, `TRANSFER` ja `ADJUSTMENT` laoliikumistega. Eraldi tuleb üle vaadata sagedaste paranduskannete ja ülekannetega tooted, sest need võivad viidata sisestusvigadele või ebatäpsele varude liikumise protsessile. Soovitan võtta kasutusele iganädalase erandite raporti, mis toob automaatselt välja negatiivse laoseisu, suured korrigeerimised ja kiiresti väheneva varuga tooted.


## Põhjalik analüüs

- [Inventuuristatistika ja kategooriate müügianalüüs minu portfoolios](https://github.com/Nordmehr/daca-portfolio/blob/main/week-4/README.md)
