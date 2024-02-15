---
title: Digital legeerklæring
nav_order: 1
layout: default
has_toc: true
has_children: true
# Index page
---

<u>Digital legeerklæring</u>
{: .fw-800 .fs-8 .lh-1 .text-center}
Pleiepenger for sykt barn
{: .fw-500 .fs-6 .lh-tight .text-center}

NAV utvikler en digital legeerklæring for pleiepenger som på sikt skal
erstatte [dagens skjema](assets/img/legeerklaering-og-veiledning-pleiepenger-sykt-barn.jpg). Den nye løsningen utvikles i
samarbeid med Helse Vest og DIPS.

## Oversikt

Pleiepenger for sykt barn er for en person som må være borte fra jobb for å være sammen med et barn som på grunn av
sykdom trenger tilsyn og pleie hele tiden. Barnet må ha vært til behandling/utredning i sykehus eller annen
spesialisthelsetjeneste. Det er ingen tidsbegrensing for hvor lenge man kan få pleiepenger når alle vilkårene er
oppfylt.

I [dag](teknisk-dokumentasjon/as-is.md) skriver lege ut en legeerklæring i EPJ og overlever denne til omsorgsperson (som
oftest foreldre) som
igjen leverer denne til NAV sammen med søknad om pleiepneger for sykt barn. Målet med den nye løsningen er at
legeerklæringen skal [sendes automatisk fra lege til NAV](teknisk-dokumentasjon/to-be.md). Men da det er en del
juridiske avklaringer som må
på
plass før vi kan lansere denne løsningen har vi besluttet å produksjonsette en midlertidig løsning:
![0-5](https://github.com/navikt/helseopplysninger-docs/assets/130694937/67a7957d-752b-449c-9d34-f35958e3ea40)
I den midlertidige løsningen vil lege skrive legeerklæring i en ny applikasjon utviklet av NAV i EPJ, og deretter
overlevere
den til omsorgsperson slik som i dag. Fordelen med den midlertidige løsningen er at alle aktører (NAV, Helse Vest og
DIPS) får erfaring med teknologien (SMART on FHIR) i produksjon, og NAV lærer mer om hva det vil bety å være en
softwareleverandør i helsesektoren.
