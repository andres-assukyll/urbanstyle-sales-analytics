# Nädal 3: SQL JOINs

## 📦 Inventuuri soovitused

**Nimi:** Nele Kund   
**Meeskond:** Sales Analytics    
**Roll:** C – Müümata toodete ja inventuuri analüüs   
**Andmeallikad:** `products` , `sales`, `inventory` tabelid (Supabase)


### 🔝 Populaarsus vs kogumüük

| Kategooria | Müüdud kogus (tk) | Kogumüük (€) |
|:---:|:---:|:---:|
| 🥇 Meeste riided | **4 121** | **749 798.72** |
| 🥈 Jalanõud | **3 737** | **774 034.75** |
| 🥉 Lasteriided | **3 686** | **305 844.45** |
| 👗 Naiste riided | **3604** | **686 464.24** |
| 💍 Aksessuaarid | **3231** | **393 035.82** |

*⚠️ Tähelepanek: Kuigi naiste riided on müüdud koguse põhjal 4. kohal, on see kogumüügilt 3. suurim tuluallikas ning toonud sisse 686 464.24 €. Turundusfookus hoida ka naisteriietel!*

✔ Müüdud koguse põhjal tasub inventuuri planeerimisel **prioritiseerida TOP 3** toodete laoseisu ja saadavust   


### 🚨 Müümata tooted

❗ Kokku on **12** müümata toodet - neid pole kordagi ostetud ega inventuuri tabelisse lisatud. Lisaks selgus, et tegemist on duplikaatsete toodetega, mis tuleks segaduse vältimiseks `products` tabelist eemaldada.


### 🚚 Laoseis

🚩 **231** toodet vajab juurdetellimist.  
*Soovitatav prioriteettsuse järjekord toodete saadavuse põhjal* :    
     **Kriitiline:** Laoseis negatiivne ➜ **Kõrge:** Laoseis 0 ➜ **Keskmine:** Positiivne, kuid ebapiisav laoseis.




