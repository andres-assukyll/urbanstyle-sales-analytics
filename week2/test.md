## MEESKOND: Sales Analytics  |  NÄDAL: 2 |  TEGELANE: Toomas Kask

---

## 👥 Meeskonnaliikmed

| Nimi | Roll (Nädal 2) | OS |
|---|---|:---:|
| [Evelyn Uusmaa](sales-data-cleaner.md) | A: Sales Data Cleaner | 🪟 Win |
| [Nele Kund](customer-data-cleaner.md) | B: Customer Data Cleaner | 🪟 Win |
| [Andres Assuküll](product-data-cleaner.md) | C: Product Data Cleaner | 🍎 Mac |

---

## 📊 Andmekvaliteedi koondraport

| Andmestik | Tulemus |
|---|---:|
| 🧾 **Sales** | **6 603** ebatäpse andmekvaliteediga müügirida eemaldatud |
| 👥 **Customers** | **[arv]** kommentaari leitud |
| 📦 **Products** | **12** duplikaatset toodet eemaldatud |

---

## 🚨 Suurim üllatus

**5 116 üleliigset duplikaatrida**  
leidus müügiandmetes.

> `invoice_id` korduvad väärtused esinesid tabelis **1 487 korral**.

See on oluline risk, sest korduvad müügiread võivad näidata tegelikust suuremat **müügitulu** ja **tellimuste arvu**.

🟢 **Hea uudis:** tooteandmed olid üpris puhtad.

---

## 💡 Soovitus Toomasele

**Peamine prioriteet: parandada duplikaatide tekkepõhjus.**

Korduvate müügiridade vältimiseks võiks `invoice_id` kordumist kontrollida juba **andmete sisestamisel**.

See aitab vähendada hilisemat puhastustööd ning vältida moonutatud müügi- ja tellimusstatistikat.

---

## ⚠️ Puuduvad andmed

| Väli | Probleem | Mõju |
|---|---|---|
| `customer_id` | Väärtus puudub | Kõiki oste ei saa kliendiga siduda |
| `sale_date` | Väärtus puudub | Müüki ei saa täielikult kasutada perioodianalüüsis |
| `total_price` | Väärtus puudub | Müüki ei saa täielikult kasutada müügitulu analüüsis |

---

### 📌 Kokkuvõte

> **🎯 Prioriteet:** peatada duplikaatide tekkimine andmete sisestamisel.  
> **⚠️ Peamine risk:** müügitulu ja tellimuste arvu kunstlik suurenemine.  
> **📊 Andmekvaliteet:** Sales ⚠️ · Customers ⚠️ · Products 🟢
