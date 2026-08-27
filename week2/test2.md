# 📊 Sales Analytics — Data Quality Report

> **Nädal 2 · Toomas Kask · Sales Data Cleaner**

---

## 👥 Meeskond

| Nimi | Roll | OS |
|---|---|:---:|
| [Evelyn Uusmaa](sales-data-cleaner.md) | A: Sales Data Cleaner | 🪟 **Win** |
| [Nele Kund](customer-data-cleaner.md) | B: Customer Data Cleaner | 🪟 **Win** |
| [Andres Assuküll](product-data-cleaner.md) | C: Product Data Cleaner | 🍎 **Mac** |

---

## 📈 Andmekvaliteedi ülevaade

![Sales](https://img.shields.io/badge/Sales-6603%20rida%20eemaldatud-orange)
![Duplicates](https://img.shields.io/badge/Duplicates-5116-red)
![Invoice IDs](https://img.shields.io/badge/Invoice%20ID-1487%20kordust-red)
![Customers](https://img.shields.io/badge/Customers-info%20tulekul-yellow)
![Products](https://img.shields.io/badge/Products-12%20duplikaati%20eemaldatud-yellow)
![Status](https://img.shields.io/badge/Status-Cleaned-success)

| Andmestik | Probleem | Tulemus |
|---|---:|---|
| 🧾 **Sales** | 6 603 ebatäpset rida | ✅ Eemaldatud |
| 🔁 **Sales duplicates** | 5 116 duplikaatrida | ⚠️ Tuvastatud |
| 🧾 **invoice_id** | 1 487 korduvat väärtust | ⚠️ Tuvastatud |
| 👥 **Customers** | [arv] kommentaari | ⚠️ Vajab ülevaatust |
| 📦 **Products** | 12 duplikaati | ✅ Eemaldatud |

---

## 🔄 Andmete puhastamise protsess

```mermaid
flowchart LR
    A[(Raw Data)] --> B[🔍 Quality Check]
    B --> C{Problems Found?}

    C -->|Yes| D[🧹 Data Cleaning]
    C -->|No| E[✅ Data Ready]

    D --> F[🔁 Remove Duplicates]
    D --> G[⚠️ Handle Missing Values]
    D --> H[🧾 Validate invoice_id]

    F --> I[(Clean Data)]
    G --> I
    H --> I

    I --> E
