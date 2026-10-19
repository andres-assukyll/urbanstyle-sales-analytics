## MEESKOND: Sales Analytics | NÄDAL: 6 | TEGELANE: Anna Mets

---

## 👥 Meeskonnaliikmed

| Nimi | Ülesanne (Nädal 6) | OS |
|---|---|:---:|
| Nele Kund | A: [Tallinna ja Tartu kaupluste andmelood](Tallinn-Tartu-stores-dashboards.md) | 🪟 Win |
| Evelyn Uusmaa | B: [Pärnu kaupluse ja e-poe dashboard'id ning andmelood](Pärnu_Epood_analüüs.md) | 🪟 Win |
| Andres Assuküll | E: [Valideerija & Kvaliteedikontroll + Ärisünteesi koondaja](vka.md) | 🍎 Mac |



## E + F : Kvaliteedikontroll ja ärisüntees

Kontrolliti **10 118** müügirida, et tagada andmete usaldusväärsus.

**Peamised leiud:**
- 0 duplikaatset ID-d.
- 988 (9,8%) müügireal puudub kliendi-ID; nendega seotud müügitulu on 286 446,20 €.
- 501 müügirea summa erineb arvutusest `quantity × unit_price` üle 0,01 € (195 negatiivset ja 306 positiivset summat).
- 10 toote jaehind on omahinnast madalam.
- Puuduvaid tooteviiteid ega müügikuupäevi ei leitud.

**Soovitused:** kontrollida müügisummade erinevusi algdokumentide alusel, selgitada negatiivsete summade tähendus, uurida puuduvaid kliendi-ID-sid ning kontrollida kahjumliku hinnastamisega tooteid. Lisada automaatsed andmekvaliteedi kontrollid.

**Järeldus:** enne müügi- ja kasumlikkuse analüüsi tuleb lahendada peamised andmekvaliteedi probleemid, et tagada usaldusväärsed äriotsused.
