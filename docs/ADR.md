---
title: ADR
layout: default
nav_order: 3
has_children: true
child_nav_order: reversed
parent: Teknisk dokumentasjon
has_toc: true
---

ADR
{: .fw-800 .fs-8 .text-center}

Denne seksjonen inneholder oversikt over alle ADR for Team Helseopplysninger.
{: .text-center }

## Bidra

Malen for ADR finner du under. Lag en ny fil i `/adr` mappen og kopier innholdet i filen. Gi filen et logisk navn med
det neste nummeret i rekkefølgen som prefiks.

```markdown
---
title: Tittel på ADR
date: 2024-01-01 # Tid kan også legges til med format HH:MM:SS +/-TTTT 
categories: [ADR] # Kan være flere, men la ADR stå

author: "Forfatter Forfattersen"

mermaid: true # Aktiver Mermaid for diagrammer
parent: ADR

nav_order: 1 # Det neste nummeret i rekkefølgen. Tilsvarer prefiks i filnavn.
---

## Status

Hva er status på denne ADR'en?

* `Akseptert`
* `Under arbeid`
* `Implementert`
* `Implementeres ikke`

## Kontekst

Bakgrunn for denne ADR'en, hvilken utfordring er det som skal løses, og/eller hvorfor er det viktig med en beslutning på
dette området

## Løsningsalternativer

Beskriv de forskjellige løsningsalternativene

| Alternativ | Fordeler | Ulemper |
|------------|----------|---------|
| ...        | ...      | ...     |
| ...        | ...      | ...     |

Ta gjerne med skisser hvis det er aktuelt

## Beslutning

Beskriv beslutningen, og om den er permanent eller midlertidig.

## Konsekvenser

Hvilke konsekvenser får beslutningen?
```
