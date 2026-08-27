# 📊 Operatsioonid — Nädal 2

> **👤 Tegelane:** Toomas Kask  
> **🎯 Roll:** Müügiandmete puhastaja · *Sales Data Cleaner*

---

## 🔎 Peamised leiud

| Andmestik | Tulemus |
|---|---:|
| 🧾 **Sales** | **6 603** ebatäpset müügirida eemaldatud |
| 👥 **Customers** | **[arv]** kommentaari leitud |
| 📦 **Products** | **12** duplikaatset toodet eemaldatud |

---

## 🚨 Suurim üllatus

**5 116 üleliigset duplikaatrida**  
leidus müügiandmetes.

> `invoice_id` korduvad väärtused esinesid tabelis **1 487 korral**.

See on oluline risk, sest duplikaatsed müügiread võivad näidata tegelikust suuremat **müügitulu** ja **tellimuste arvu**.

🟢 **Hea uudis:** tooteandmed olid üpris puhtad.

---

## 💡 Soovitus Toomasele

**1. Kõigepealt lahendada duplikaatide tekkepõhjus.**

Korduvate müügiridade vältimiseks võiks `invoice_id` unikaalsust kontrollida juba **andmete sisestamisel**.

See vähendaks hilisemat puhastustööd ning aitaks vältida moonutatud müügi- ja tellimusstatistikat.

---

## ⚠️ Puuduvad andmed

- `customer_id` puudumisel ei saa kõiki oste kliendiga siduda.
- `sale_date` puudumisel ei saa müüki täielikult kasutada perioodianalüüsis.
- `total_price` puudumisel ei saa müüki täielikult kasutada müügitulu analüüsis.

---

### 📌 Kokkuvõte

> **Peamine prioriteet:** peatada duplikaatide tekkimine andmete sisestamisel.  
> **Peamine risk:** müügitulemuste kunstlik suurenemine.  
> **Andmekvaliteet:** Sales ⚠️ · Customers ⚠️ · Products 🟢
