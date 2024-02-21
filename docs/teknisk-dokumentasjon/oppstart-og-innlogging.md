---
layout: default
nav_order: 1
parent: Teknisk dokumentasjon
---
# Oppstart og innlogging

```mermaid
sequenceDiagram
    participant EPJ as DIPS Arena
    participant Browser as Integrert Nettleser
    participant App as k9-legeerklaering-on-fhir-klient
    participant App-Backend as k9-legeerklaering-on-fhir-server
    participant AuthServer as DIPS Autorisasjonsserver
    participant FHIR as DIPS FHIR API

    EPJ->>Browser: A: Start webapplikasjon med SMART App Launch Framework
    Browser->>EPJ: B: Opprett LaunchContext (inkl. patient, practitioner, encounter)
    EPJ-->>Browser: B: Returner LaunchContext ID
    Browser->>App: C: Initier launch-sekvens (iss, launch)
    App->>AuthServer: D: Forespør /metadata/ eller .well-known/smart-configuration.json
    AuthServer-->>App: D: Returner URLs til authorize og token endepunkter
    App->>AuthServer: E: Forespørsel mot authorize endepunkt med nødvendige parametere
    AuthServer->>EPJ: E: Sjekk autorisasjon (lokale tilgangsregler, brukers samtykke)
    EPJ-->>AuthServer: E: Autorisasjonsavgjørelse
    AuthServer-->>App: E: Returner autorisasjonskode eller feilkode/-respons
    App->>AuthServer: F: Veksle inn autorisasjonskoden for tilgangstoken
    AuthServer-->>App: F: Returner tilgangstoken (og potensielle andre tokens som id_token, refresh_token)
    App->>App-Backend: G: Forespørsler for helsedata med tilgangstoken
    App-Backend->>FHIR: G: Forespørsler for helsedata med tilgangstoken
    FHIR-->>App-Backend: G: Returner helsedata basert på token og forespørsel
    App-Backend-->>App: G: Returner helsedata basert på token og forespørsel
```

[Mermaid Live Editor](https://mermaid.live/edit#pako:eNqdVV1vIjcU_StXfkqlGQJN-IgfViJLaKl22yi0faiQKoe5DI499tT2hM1G-Tn9D_ueP9brYYBJSPqwvIDNucfnnnNlP7KlzZBx5vGfCs0SJ1LkThQLA_QphQtyKUthAlxd_wLCw2R2PYexQyOOIZfObjy6CJuZgLlDF-BXDEEjbR_jx2UZseoi1ZgjOqUFOmny1Jp0tZYuVVqiCW8WppdiqdBk_09Ax96_eXIV1vP6v0NPVbBOeuHvrPHv1U1_nt3sK-rF-Hq2MFsgOZR--NCYwGHMYR6oFjZ4K8pSS1VzQ4EZzD-Pb36v-_8kKrNcw5Q8x411akvVkBAdkXK45PBbWTpyssF_tOTvlwAn0ijdIYkhGpVA6cQyyCCtQZcA5WkrArofDgLbCon2BkPlCPyKdzZ5rYO0cvjIKViiJ7yu8WSwukfjSYj3SbPZnBZDorq90xwmHKbWoS-fvzk4LTCITARxCqg1MXY29J0qYzfm1BdkXLq0ZiXzyonYUOfO28boA2e6UzZptfLHzScPQWoQhKNMvyLYHIKlcSFLMiwro8Iu3WOVVy2VHjUUNrSY9gR1jub5W0b9ZzLHOCeUIRHjkcomRmKe36FSkW4_a3CirRIao-JcmNw7zHVM79ZVCp0HL4rwoBS-DPGV4hfTK-7zOxKP2uO7hl21DGvL8YrugyaRFUodl6dptIP-e8-yKYc_UXlqQhpzTGdgZd2-vzqId3VNW7peVMAJhVjaQNMmozwQJnO4jZVMsgXI7O96lYDDFSleb5cvx_Fwc3D4qZ103TDJXEfb4lzWAb8l-kBBhPES-F6mWJu-IWpvwIHhVvh4mZbP_zaDTGasWlN6LG1n6PfxsYQV6AohM3obHiP7goU1FrhgnH5muBKVDgu2ME8EjYnPH8yS8eAqTFhV0iG7p4TxlaBjd7tXmaTx2G_StfqXtUV7zfgj-8J42huMOv3RYNAfdkfDs4teL2EPjP_YO-v0z7vnF4PuaNTr9Z4S9rUm6HZGg7OLYfe8P-p3h_2z4ShhWB_2efvE1S_d038pJmoc)
