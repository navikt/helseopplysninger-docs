---
title: Digital legeerklæring
nav_order: 1
layout: default
has_toc: true
has_children: true
# Index page
---

# Digital legeerklæring - pleiepenger for sykt barn

NAV utvikler en digital legeerklæring for pleiepenger som på sikt skal
erstatte [dagens skjema](assets/img/legeerklaering-og-veiledning-pleiepenger-sykt-barn.jpg). Den nye løsningen utvikles i
samarbeid med [Helse Vest](https://www.helse-vest.no/) og [DIPS](https://www.dips.com/).

Mer informasjon om pleiepenger for sykt barn finnes på [nav.no](https://www.nav.no/pleiepenger-barn), og i [folketrygdlovens kapittel 9](https://lovdata.no/pro/lov/1997-02-28-19/§9-10).

Pleiepenger for sykt barn er en stønadsordning for omsorgspersoner som må være borte fra jobb for å ta vare på et barn som trenger kontinuerlig tilsyn og pleie på grunn av sykdom. Barnet må ha vært til behandling eller utredning i sykehus eller annen spesialisthelsetjeneste, og det er ingen tidsbegrensning for hvor lenge man kan motta pleiepenger når alle vilkårene er oppfylt.

I [dag](funksjonell-dokumentasjon/as-is.md) benyttes en manuell prosess hvor leger utsteder legeerklæringer i EPJ-systemer. Disse erklæringene overleveres deretter til omsorgspersoner, vanligvis foreldre, for videre levering til NAV i forbindelse med søknader om pleiepenger for sykt barn. [Målet](funksjonell-dokumentasjon/to-be.md) med den nye løsningen er å automatisere denne prosessen ved å etablere en direkte elektronisk overføring av legeerklæringen fra legen til NAV. Dette vil effektivisere og forenkle søknadsprosessen betydelig, og samtidig sikre raskere og mer nøyaktig behandling av søknader om pleiepenger for sykt barn.

Men da det er en del juridiske avklaringer som må på plass før vi kan lansere denne løsningen har vi besluttet å produksjonsette en [midlertidig løsning](funksjonell-dokumentasjon/0-5.md).

![0-5](https://github.com/navikt/helseopplysninger-docs/assets/130694937/67a7957d-752b-449c-9d34-f35958e3ea40)

I den midlertidige løsningen vil legene bruke en ny applikasjon utviklet av NAV i EPJ-systemene til å utstede legeerklæringer. Deretter vil disse erklæringene overleveres til omsorgspersonene på samme måte som i dag. Fordelen med den midlertidige løsningen er at alle involverte aktører, inkludert NAV, Helse Vest og DIPS, får erfaring med den nye teknologien, SMART on FHIR, i produksjonsmiljøet. Samtidig vil NAV oppnå verdifull innsikt i hva det innebærer å være en programvareleverandør i helsetjenesten.

Den midlertidige løsningen vil gi oss verdifull læring og erfaring som vi kan dra nytte av når den automatiserte løsningen implementeres. Vi vil fortsette å jobbe med juridiske aspekter og tekniske detaljer for å sikre en smidig overgang til den endelige løsningen som vil effektivisere informasjonsutvekslingen mellom helsetjenesten og NAV.

Vi er forpliktet til å sikre en sømløs og sikker informasjonsutveksling som oppfyller kravene til personvern og juridiske bestemmelser, samtidig som vi legger til rette for en mer effektiv og brukervennlig prosess for alle involverte parter.
