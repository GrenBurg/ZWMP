# Zendweg Multiplayer

Trainingssim voor beginnende satcom-operators, voor twee spelers. De ene speler bedient het grondstation (DMD2050E in L-band, met spectrum analyzer), de andere de CCT200 in het veld (Ku). Samen bouwen ze een link op via SES-4 (transponder EUV05 of EUV09).

**Openen:** https://grenburg.github.io/ZWMP/

## Koppelen

De browsers praten direct met elkaar via WebRTC. Er is geen server, account of API-key nodig.

1. Grondstation: kies de rol en klik **Maak sessiecode**. Stuur de code (±120 tekens) naar de CCT200-speler.
2. CCT200: plak de sessiecode, klik **Maak antwoordcode** en stuur die terug.
3. Grondstation: plak de antwoordcode en klik **Verbinden**.

Op één netwerk werkt dit ook zonder internet. Over het internet vraagt elke browser eenmalig zijn publieke adres op bij een publieke STUN-server. Een strenge firewall kan de directe verbinding blokkeren.

Solo spelen kan ook: dan staan beide modems op één scherm.

## Versies

| Versie | Wijziging |
|---|---|
| v1.0 | Eerste multiplayerversie, gebouwd op SES-4 Zendweg Lab v1.8 |
