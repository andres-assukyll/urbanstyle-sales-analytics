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
1. "Kui palju aega pipeline kokku hoiab, võrreldes käsitsi töötlusega?"
   Mõtelge, kui kaua võiks sama töötlus käsitsi aega võtta (andmete laadimine, puhastamine, analüüs, eksport) — ja kui kaua pipeline seda teeb.
2. "Milline soovitus Markole automatiseerimise laiendamiseks?"
   Mida veel võiks automaatselt teha? Churn risk alert? Inventory warning? Weekly email?
3. "Mis juhtub, kui Supabase on maas? Kuidas meie pipeline sellega toime tuleb?"
   Kas pipeline crash'ib? Kas on fallback? Kuidas veakäsitlus aitab?
   - Supabase'i ajutise tõrke korral kasutab meie pipeline *retry* mehhanismi. Pärast kolme ebaõnnestunud katset edastatakse viga pipeline'ile, mis omakorda ei jätka puudulike andmetega, vaid märgib vastava perioodi ebaõnnestunuks. Mitme perioodi korral saab pipeline seetõttu teisi perioode siiski töödelda ning lõpptulemusena saadetakse üks staatusepõhine e-kiri. <br>
   - *Fallback*i ehk asendusandmeallikat hetkel ei kasutata.

## 📧 *Pipeline* e-kirja teavitus

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
