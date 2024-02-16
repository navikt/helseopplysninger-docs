---
title: "Målbilde"
layout: default
nav_order: 3
parent: Digital legeerklæring
---

# Målbilde

{: .highlight }
Det er i skrivende stund ikke avklart hvordan den endelige løsningen vil bli. Det gjenstår juridiske avklaringer, alt som står på denne siden må derfor sees på som et utkast.

## Dataflyt
![to-be](https://github.com/navikt/helseopplysninger-docs/assets/130694937/c8c62ce4-715d-49d3-a969-afcf54b45d37)

1. En lege i spesialisthelsetjenesten, for eksempel på et sykehus, skriver en legeerklæring når det er relevant for omsorgspersoner, som vanligvis er foreldre, å søke om pleiepenger for et sykt barn. Årsakene til at legeerklæringen fylles ut kan variere og inkluderer rutinemessig utfylling ved innleggelse på nyfødtintensiven, forespørsler fra foreldre, helsepersonell som sosionomer, eller andre årsaker som ikke nødvendigvis er kjent.

2. Legeerklæringen fylles ut av legen i NAVs SMART on FHIR applikasjon som er sømløst integrert i EPJ. Applikasjonen henter data om pasient, lege og sykehus fra EPJ, og journalfører legerklæringen tilbake til EPJ som en PDF etter at lege har dokumentert pleiebehov, diagnosekoder og tidsperiode. 

3. Legerklæringen sendes elektronisk fra EPJ til NAV uten at omsorgsperson er involvert. (Trenger juridiske avklaringer)

4. Omsorgspersonen søker deretter om pleiepenger hos NAV og søknaden kobles sammen med relevant legeerklæring, og det opprettes en sak på på søker. (Trenger juridiske avklaringer)

5. Saksbehandler i NAV får tilgang til legeerklæringen ved saksbehandling av søkers sak.
