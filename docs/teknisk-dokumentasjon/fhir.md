---
layout: default
nav_order: 2
parent: Teknisk dokumentasjon
---
# FHIR kall mot EPJ

TODO: Oversikt over alle FHIR kall mot EPJ

## Opplysningstyper
Detaljert informasjonsmodel finnes i [HelseopplysningerTypes.ts](https://github.com/navikt/k9-legeerklaering-on-fhir/blob/main/src/integrations/helseopplysningerserver/types/HelseopplysningerTypes.ts)

| Kategori              | Element                    | Token          | FHIR |
|:----------------------|:---------------------------|:---------------|:------------|
| Lege                  | fornavn                    | dips-firstname | 
| Lege                  | etternavn                  | dips-lastname  | Innlogget leges etternavn |
| Lege                  | hpr                        | hpr-nummer     | Innlogget leges HPR-nummer |
| Sykehus               | navn                       | Ja          | Sykehusets navn |
| Sykehus               | telefonnummer              | Ja          | Sykehusets telefonnummer |
| Sykehus               | adresse/gateadresse        | Ja          | Sykehusets adresse |
| Sykehus               | adresse/gateadresse2       | Ja          | Sykehusets adresse |
| Sykehus               | adresse/postkode           | Ja          | Sykehusets postnummer |
| Sykehus               | adresse/by                 | Ja          | Sykehusets poststed |
| Pasient               | navn                       | Ja          | Pasientens navn |
| Pasient               | id                         | Ja          | Pasientens person- eller d-nummer |
| Pasient               | fødselsdato                | Ja          | Pasientens fødselsdato |
| Legens vurdering      | vurderingAvBarnet          | Nei         | Legens vurdering av barnets tilstand. Inneholder medisinske tilstand, funksjonsnivå, behovet for kontinuerlig tilsyn og pleie, samt sykdomsutvikling og prognose. |
| Legens vurdering      | vurderingAvOmsorgspersoner | Nei         | Legens vurdering av om det er behov én eller to personer samtidig for å pleie og/eller ha tilsyn med barnet når barnet er hjemme. |
| Diagnosekode          | hoveddiagnose              | Nei         | [ICD-10](https://www.ehelse.no/kodeverk-og-terminologi/ICD-10-og-ICD-11) diagnosekode. |
| Diagnosekode          | bidiagnose(r)              | Nei         | [ICD-10](https://www.ehelse.no/kodeverk-og-terminologi/ICD-10-og-ICD-11) diagnosekoder. |
| Innleggelse(r)        | fom                        | Nei         | Periode(r) for innleggelse(r) på helseinstitusjon (fra dato)  |
| Innleggelse(r)        | tom                        | Nei         | Periode(r) for innleggelse(r) på helseinstitusjon (til dato)  | 
| Tilsyn- og pleiebehov | fom                        | Nei         | Forventet varighet på tilsyns- og pleiebehovet (fra dato) |
| Tilsyn- og pleiebehov | tom                        | Nei         | Forventet varighet på tilsyns- og pleiebehovet (till dato) |
