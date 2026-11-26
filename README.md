# Zendweg Multiplayer

Trainingssim voor beginnende satcom-operators, voor twee spelers. De ene speler bedient het grondstation (DMD2050E in L-band, met spectrum analyzer), de andere de CCT200 in het veld (Ku). Samen bouwen ze een link op via SES-4 (transponder EUV05 of EUV09).

**Openen:** https://grenburg.github.io/ZWMP/

## Koppelen

1. Kies je rol: **Grondstation** of **CCT200**.
2. Vul allebei dezelfde **sessienaam** in (bijvoorbeeld `LES-3A`), eventueel met een wachtwoord, en klik **Verbinden**.
3. Zodra de andere rol in dezelfde sessie zit, staan jullie gekoppeld.

De koppeling loopt via de Ably-relay over gewoon HTTPS. Daardoor werkt hij ook in getunnelde werkomgevingen waar WebRTC uitstaat. De berichten zijn versleuteld met een sleutel die uit sessienaam en wachtwoord wordt afgeleid. De Ably-key in de pagina mag alleen publiceren, abonneren en aanwezigheid melden op kanalen `zwmp:*`.

**Handmatig koppelen met codes** blijft beschikbaar als reserve. Dat is een directe WebRTC-verbinding zonder relay, en werkt alleen waar WebRTC aanstaat.

Solo spelen kan ook: dan staan beide modems op één scherm.

## RF Lab

Bovenin kies je tussen **Zendweg Multiplayer** en **RF Lab**; het gekozen onderdeel staat in grote letters. RF Lab (`rflab.html`, direct te openen via `#rflab`) laat golfvorm, constellatie, spectrum en linkbudget zien voor X-, Ku- en Ka-band, met modemmodes van de DMD2050E en SLM-5650A uit de Comtech EF Data-datasheets, of generiek. Een lopende koppeling in de zendweg blijft actief terwijl je in RF Lab werkt.

`ably.min.js` is de Ably JavaScript SDK 2.27.0 (Apache-2.0), meegeleverd zodat de pagina niet van een externe CDN afhangt.

## Versies

| Versie | Wijziging |
|---|---|
| v1.0 | Eerste multiplayerversie, gebouwd op SES-4 Zendweg Lab v1.8 |
| v1.1 | Koppelen via sessienaam over de Ably-relay (HTTPS); handmatige codes blijven als reserve |
| v1.2 | BurgFunk-logo in de kop en als favicon |
| v1.3 | Weer per locatie (6 situaties) en ruimtestorm; willekeurig verloop of handmatig te kiezen |
| v1.4 | RF Lab (voorheen SHF Modulation Lab) toegevoegd; bovenin kiezen tussen Zendweg en RF Lab |
