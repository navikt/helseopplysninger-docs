# FHIR kall mot EPJ
## Patient
### Request
|Key|Value|
|---|---|
|Metode|GET|
|URL (eksempel)| https://api.dips.no/fhir/patient/cdp2019153|
|Request parameter: cdp2019153|Hentes fra token.patient|
### Response
|Element|system|Beskrivelse|Bruk|
|---|---|---|---|
|identifier-value|urn:oid:2.16.578.1.12.4.1.4.3|Pasientens fødselsnummer|Vises i applikasjon etter pasientens navn, lagres i PDF|
## PractitionerRole
