## MEESKOND: Sales Analytics  |  NÄDAL: 2 |  TEGELANE: Toomas Kask

---

## 👥 Meeskonnaliikmed

| Nimi | Roll (Nädal 2) | OS |
|---|---|:---:|
| [Evelyn Uusmaa](sales-data-cleaner.md) | A: Sales Data Cleaner | 🪟 Win |
| [Nele Kund](customer-data-cleaner.md) | B: Customer Data Cleaner | 🪟 Win |
| [Andres Assuküll](product-data-cleaner.md) | C: Product Data Cleaner | 🍎 Mac |

---

## 📈 Andmekvaliteedi koondraport
![Sales](https://img.shields.io/badge/Sales-6603%20rida%20eemaldatud-red)
![Customers](https://img.shields.io/badge/Customers-info%20tulekul-orange)
![Products](https://img.shields.io/badge/Products-12%20duplikaati%20eemaldatud-yellow)
![Status](https://img.shields.io/badge/Status-Cleaned-success)

| Andmestik | Tulemus |
|---|---|
| 🧾 **Sales** | **6 603** ebatäpse andmekvaliteediga müügirida eemaldatud |
| 👥 **Customers** | **[arv]** kommentaari leitud |
| 📦 **Products** | **12** duplikaatset toodet eemaldatud |

---

### 🚨 Suurim üllatus

Müügiandmetes leidus **5 116 üleliigset duplikaatrida**.  <br>
Korduvaid `invoice_id` väärtusi esines tabelis **1 487 korral**. <br>
See on oluline risk, sest korduvad müügiread võivad näidata tegelikust suuremat **müügitulu** ja **tellimuste arvu**.

🟢 **Hea uudis:** tooteandmed olid üpris puhtad.

---

### 💡 Soovitus Toomasele
🎯 **Peamine prioriteet: parandada duplikaatide tekkepõhjus.** <br>
Andmete (nt `invoice_id`, `product_id`jne) kordumisi tuleks kontrollida juba **andmete sisestamisel**.

See aitab: <br>
- vältida topeltmüüke;
- hoida müügitulu õigena;
- vähendada hilisemat puhastustööd;
- parandada perioodi- ja müügitulemuste analüüsi.

---

### ⚠️ Puuduvad andmed
| Väli          | Probleem           | Mõju analüüsile                         |
| ------------- | ------------------ | --------------------------------------- |
| `customer_id` | Puuduvad väärtused | ❌ Kõiki oste ei saa kliendiga siduda |
| `sale_date`   | Puuduvad väärtused | ❌ Müüki ei saa täielikult kasutada perioodianalüüsis |
| `total_price` | Puuduvad väärtused | ❌ Müüki ei saa täielikult kasutada müügitulu analüüsis |

---

## 📌 Kokkuvõte

> **🎯 Prioriteet:** peatada duplikaatide tekkimine andmete sisestamisel.  
> **⚠️ Peamine risk:** müügitulu ja tellimuste arvu kunstlik suurenemine.  
> **📊 Andmekvaliteet:** Sales ⚠️ · Customers ⚠️ · Products 🟢


