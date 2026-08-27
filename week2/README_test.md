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
![Customers](https://img.shields.io/badge/Customers-520%20probleemi%20leitud-orange)
![Products](https://img.shields.io/badge/Products-12%20duplikaati%20eemaldatud-brightgreen)
![Status](https://img.shields.io/badge/Status-vajab%20täiendamist-yellow)

| Andmestik | Tulemus |
|---|---|
| 🧾 **Sales** | **6 603** ebatäpse andmekvaliteediga müügirida eemaldatud |
| 👥 **Customers** | **520** kliendiandmetega seotud probleemi leitud |
| 📦 **Products** | **12** duplikaatset toodet eemaldatud |

---

### 🚨 Suurim üllatus

Müügiandmetes **5 116 üleliigset duplikaatrida**. Korduvaid `invoice_id` väärtusi **1 487**. <br> 
*See on oluline risk, sest korduvad müügiread võivad näidata tegelikust suuremat **müügitulu** ja **tellimuste arvu**.*

Kliendiandmetes puuduvaid e-poste **380** ja korduvaid **128**. <br>
*Tekitab probleemseid kliendikontakte (nt tellimuse kinnitamine, teavitamine, turunduskampaaniad jms).*

🟢 **Hea uudis:** tooteandmed olid üpris puhtad. <br>

---

### 💡 Soovitus Toomasele
🎯 **Peamine prioriteet: parandada duplikaatide ja puuduvate andmete tekkepõhjus.** <br>
Andmete (nt `invoice_id`, `email`, `product_id`jms) kordumisi ja puudumisi tuleks kontrollida juba **andmete sisestamisel**.

 **See aitab:** <br>
🔸 vältida topeltmüüke; <br>
🔸 tagada andmete kvaliteedi; <br>
🔸 vähendada puhastustööd; <br>
🔸 parandada analüüsi täpsust.

---

### ⚠️ Puuduvad andmed
| Väli          | Probleem           | Mõju analüüsile                         |
| ------------- | ------------------ | --------------------------------------- |
| `customer_id` | Puuduvad väärtused | ❌ Kõiki oste ei saa kliendiga siduda |
| `sale_date`   | Puuduvad väärtused | ❌ Müüki ei saa täielikult kasutada perioodianalüüsis |
| `total_price` | Puuduvad väärtused | ❌ Müüki ei saa täielikult kasutada müügitulu analüüsis |

---

#### 📌 Kokkuvõte

> **🎯 Prioriteet:** peatada duplikaatide tekkimine andmete sisestamisel.  
> **⚠️ Peamine risk:** müügitulu ja tellimuste arvu kunstlik suurenemine.  
> **📊 Andmekvaliteet:** Sales ⚠️ · Customers ⚠️ · Products ⭐


