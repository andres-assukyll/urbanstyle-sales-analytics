# Roll A – API päringud ja automatiseerimine

**Autor:** Evelyn Uusmaa

## Minu panus

- Koostasin Supabase API kaudu müügi-, kliendi- ja tooteandmete pärimise funktsioonid.
- Lisasin andmete laadimise 1000 rea kaupa ja päringuvigade edasiandmise.
- Võimaldasin müügiandmeid filtreerida kuupäevavahemiku järgi.
- Koostasin esialgse pipeline’i koos logimise, andmekontrollide ja töö kestuse mõõtmisega.

Kuupäevavahemiku saab anda pipeline’i käivitamisel terminalist.
Uue perioodi töötlemiseks ei ole vaja koodi muuta:
kuupäevad edastatakse fetcherile ning filter rakendatakse API-päringus.

## Minu failid

- [data_fetcher_e.py](src/data_fetcher_e.py)
- [pipeline2.py](src/pipeline2.py)

## Käivitamine

Käivita `src` kaustas:

```powershell
python pipeline2.py --start-date 2023-01-01 --end-date 2023-01-31
```

## Kontrolli tulemused

Jaanuari 2023 päring tagastas 261 müügirida.
Klienditabelis oli 3150 ja tootetabelis 362 rida.

## Meeskonna täiendused

Korduskatsed, `config.yaml`, mitme perioodi töötlemine ja
e-posti teavitused lisas meeskonnakaaslane ühisesse lõppversiooni.
