# Nädal 1: SQL Basics
## 📊 Sales Data Explorer

**Meeskond:** Sales Analytics  
**Roll:** A – Sales Data Explorer  
**Andmeallikas:** ´sales tabel´ (Supabase)

---

## 📌 Kokkuvõte

| Näitaja | Tulemus |
|---|---:|
| Ridu | 15 234 |
| Veergusid | 12 |
| Suurim tehing | 2 170,40 |
| Väikseim tehing | -1 405,32 |
| Puuduv kliendiinfo | 1 487 (~9,76%) |

**Veerud (12):**  
`id` · `sale_id` · `invoice_id` · `sale_date`  
`customer_id` · `product_id` · `quantity` · `unit_price`  
`total_price` · `channel` · `store_location` · `payment_method`

## 🔎 Mis oli üllatav?

Andmestikus esineb negatiivseid tehinguid.

> Kas tegemist on tagastustega?  
> Kuidas arvestada neid edasises analüüsis?

## 💡 Järeldused

Sales tabel annab hea aluse edasiseks andmeanalüüsiks, kuid enne tuleks selgitada:
- negatiivsete tehingute tähendus;
- puuduva kliendiinfo põhjus.
