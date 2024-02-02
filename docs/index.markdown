# Digital legeerklæring: pleiepenger for sykt barn

NAV utvikler en digital legeerklæring for pleiepenger som på sikt skal
erstatte [dagens skjema](resources/legeerklæring-og-veiledning-pleiepenger-sykt-barn.jpg). Den nye løsningen utvikles i
samarbeid med Helse Vest og DIPS.

### Innholdsfortegnelse

* [Digital legeerklæring](#digital-legeerklæring-pleiepenger-for-sykt-barn)
    * [Oversikt](#oversikt)
    * [Support](#support)
* [Eksisterende prosess](as-is.md)
* [Fremtidig løsning](to-be.md)
* [Teknisk dokumentasjon](tekniskEKNISK.md)
* [ADR](adrDR.md)

## Oversikt

Pleiepenger for sykt barn er for en person som må være borte fra jobb for å være sammen med et barn som på grunn av
sykdom trenger tilsyn og pleie hele tiden. Barnet må ha vært til behandling/utredning i sykehus eller annen
spesialisthelsetjeneste. Det er ingen tidsbegrensing for hvor lenge man kan få pleiepenger når alle vilkårene er
oppfylt.

I [dag](as-is.md) skriver lege ut en legeerklæring i EPJ og overlever denne til omsorgsperson (som oftest foreldre) som
igjen leverer denne til NAV sammen med søknad om pleiepneger for sykt barn. Målet med den nye løsningen er at
legeerklæringen skal [sendes automatisk fra lege til NAV](to-be.md). Men da det er en del juridiske avklaringer som må
på
plass før vi kan lansere denne løsningen har vi besluttet å produksjonsette en [midlertidig løsning](0-5.md). I den
midlertidige løsningen vil lege skrive legeerklæring i en ny applikasjon utviklet av NAV i EPJ, og deretter overlevere
den til omsorgsperson slik som i dag. Fordelen med den midlertidige løsningen er at alle aktører (NAV, Helse Vest og
DIPS) får erfaring med teknologien (SMART on FHIR) i produksjon, og NAV lærer mer om hva det vil bety å være en
softwareleverandør i helsesektoren.

## Support

NAV ansatte kan kontakte teamet på [#team-helseopplysninger](https://app.slack.com/client/T5LNAMWNA/C01AQTAU3CH),
eksterne kan sende en epost til <erik.haug@nav.no>