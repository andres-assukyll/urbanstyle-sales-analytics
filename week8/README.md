## MEESKOND: Sales Analytics | NÄDAL: 8 | TEGELANE: Marko Saar

---

## 👥 Meeskonnaliikmed

| Nimi | Ülesanne (Nädal 7) | OS |
|---|---|:---:|
| Evelyn Uusmaa | A: [API Query + Automation](api_automation.md) | 🪟 Win |
| Andres Assuküll | B: [Data Processing](data.md) | 🍎 Mac  |
| Nele Kund | C: [Visualization + Saving](visual_saving.md) | 🪟 Win |

## ❓ Küsimused
Meeskond arutab ja vastab kolmele küsimusele (vastused suunatakse Markole):
#### Kui palju aega pipeline kokku hoiab, võrreldes käsitsi töötlusega?

Hinnanguliselt võtaks samade andmete käsitsi laadimine, puhastamine, analüüs ja visualiseerimine u. 55–100 minutit ühe pipeline jooksutamise kohta. Automatiseeritud pipeline teeb sama töö u. 2–5 minutiga, sõltuvalt andmemahtudest ja Supabase'i ühenduse kiirusest. Seega säästab pipeline hinnanguliselt umbes 50–95 minutit ühe jooksutamise kohta ning vähendab oluliselt ka käsitsi tehtavate vigade riski. Kui aga pipeline'i käivitada kord nädalas, võib aastane ajavõit olla ligikaudu 40–80 tundi.

#### Milline soovitus Markole automatiseerimise laiendamiseks? Mida veel võiks automaatselt teha? Churn risk alert? Inventory warning? Weekly email?

Mõistlikuim edasine samm oleks laiendada automatiseerimist **Weekly Performance Email** ja **Churn Risk Alert**'idega. Pipeline võiks kord nädalas arvutada peamised KPI-d, võrrelda neid eelmise perioodiga ning tuvastada kliendid, kelle ostuaktiivsus on langenud. <br>
Need raportid kasutavad juba olemasolevaid andmeid ega nõua tingimata uut andmeallikat. Samuti liiguks projekt siis edasi **ärilise otsustoe automatiseerimise** suunas.

Lisaks võiks kaaluda ka: <br>
1. **Inventory Warning** – raportid annavad märku kiiresti vähenevast laovarust.
2. **Revenue Anomaly Alert** mõlemat tüüpi kõrvalekaldega: <br>
    📉 ebatavaliselt väike tulu — võimalik probleem müügis, andmetes või süsteemis;<br>
    📈 ebatavaliselt suur tulu — võimalik väga edukas müügipäev, kampaania mõju või anomaalia andmetes.

#### Mis juhtub, kui Supabase on maas? Kuidas meie pipeline sellega toime tuleb? Kas ta crash'ib? Kas on fallback? Kuidas veakäsitlus aitab?

| Küsimus | Meie lahendus |
|---|---|
| Supabase on korraks maas | **Retry 3×** |
| Retryde vahe | **30 sekundit** |
| Retry seadistus | `config.yaml` |
| Kui kõik retry'd ebaõnnestuvad | Viga antakse pipeline'ile |
| Kas pipeline crashib kontrollimatult? | **Ei** |
| Kas vigaste andmetega jätkatakse? | **Ei** |
| Kas on asendusandmeallikas (fallback)? | **Ei, praegu mitte** |
| Mitme perioodi korral üks periood failib | Teised võivad jätkuda |
| Mõni periood õnnestub, mõni ebaõnnestub | **WARNING** |
| Kõik perioodid ebaõnnestuvad | **FAILURE** |
| Kas saadetakse teavitus? | **Jah, üks e-mail kogu jooksu kohta** |

#### 📧 *Pipeline* e-kirja teavitus SUCCESS

✅ UrbanStyle pipeline valmis!

UrbanStyle pipeline tulemused

━━━━━━━━━━━━━━━━━━━━ <br>
📅 2023-01-01 – 2023-01-31
<br><br>
💰 Kogutulu: €79,735.03<br>
👥 Unikaalsed kliendid: 217<br>
🛒 Keskmine tellimuse väärtus: €305.50<br><br>

📁 Tulemused: /output/2023-01-01_2023-01-31<br>
━━━━━━━━━━━━━━━━━━━━<br>
📅 2023-03-01 – 2023-03-31<br><br>

💰 Kogutulu: €91,499.55<br>
👥 Unikaalsed kliendid: 283<br>
🛒 Keskmine tellimuse väärtus: €266.76<br><br>

📁 Tulemused: /output/2023-03-01_2023-03-31<br>
━━━━━━━━━━━━━━━━━━━━<br>
📅 2023-05-01 – 2023-05-31<br><br>

💰 Kogutulu: €95,316.25<br>
👥 Unikaalsed kliendid: 277<br>
🛒 Keskmine tellimuse väärtus: €277.89<br><br>

📁 Tulemused: /output/2023-05-01_2023-05-31<br>
━━━━━━━━━━━━━━━━━━━━<br>
