---
layout: default
nav_order: 2
parent: Teknisk dokumentasjon
---
# FHIR kall mot EPJ

## Patient

### Request

| Key                         | Value                                          |
|-----------------------------|------------------------------------------------|
| Metode                      | GET                                            |
| URL (eksempel)              | https://api.dips.no/fhir/patient/              |
| Query parameter: identifier | Hentes fra token.patient, eksempel: cdp2019153 |

Hvis man kaller API'et med identifier som query parameter vil man få returnert en `Bundle`, men hvis man gjør GET
direkte med id som en del av url (https://api.dips.no/fhir/patient/cdp2019153) returneres en `Patient`.

### Response

| Element          | system                        | Beskrivelse              | Bruk                                                    |
|------------------|-------------------------------|--------------------------|---------------------------------------------------------|
| identifier-value | urn:oid:2.16.578.1.12.4.1.4.3 | Pasientens fødselsnummer | Vises i applikasjon etter pasientens navn, lagres i PDF |

## PractitionerRole
