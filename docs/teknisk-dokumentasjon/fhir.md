---
layout: default
nav_order: 2
parent: Teknisk dokumentasjon
---
# FHIR kall mot EPJ
{: .no_toc }

### Innholdsfortegnelse
{: .no_toc }

- TOC
{:toc}

## Patient.GET
Benyttes for å hente informasjon om aktiv pasient i EPJ. ID til kommer som launch-paremter i oppstartssekvensen til SMART on FHIR. 
```json
{
    "resourceType": "Patient",
    "id": "cdp2019153",
    "meta": {
        "profile": [
            "DIPSPatient",
            "NoBasisPatient"
        ]
    },
    "identifier": [
        {
            "use": "temp",
            "system": "urn:oid:2.16.578.1.12.4.1.4.3",
            "value": "02512351754"
        },
        {
            "system": "http://dips.no/fhir/namingsystem/dips-patientid",
            "value": "2019153"
        }
    ],
    "active": true,
    "name": [
        {
            "use": "official",
            "text": "Fjellkjede, Betydelig",
            "family": "Fjellkjede",
            "given": [
                "Betydelig"
            ]
        }
    ],
    "gender": "male",
    "birthDate": "2023-11-02",
    "deceasedBoolean": false,
    "address": [
        {
            "extension": [
                {
                    "extension": [
                        {
                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPatientMunicipality",
                            "valueCoding": {
                                "system": "urn:oid:2.16.578.1.12.4.1.1.3402",
                                "code": "1519",
                                "display": "Volda"
                            }
                        }
                    ],
                    "url": "http://hl7.no/fhir/StructureDefinition/no-basis-propertyinformation"
                },
                {
                    "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPatientStateName",
                    "valueString": "MØRE OG ROMSDAL"
                },
                {
                    "url": "http://hl7.no/fhir/StructureDefinition/no-basis-address-official",
                    "valueBoolean": false
                }
            ],
            "use": "home",
            "line": [
                "Velsvikvegen 751"
            ],
            "city": "Lauvstad",
            "district": "Volda",
            "_district": {
                "extension": [
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPatientMunicipality",
                        "valueCoding": {
                            "system": "urn:oid:2.16.578.1.12.4.1.1.3402",
                            "code": "1519",
                            "display": "Volda"
                        }
                    }
                ]
            },
            "state": "15",
            "postalCode": "6133",
            "country": "Norge"
        }
    ]
}
```

## PractitionerRole.getCurrentUser
Henter informasjon om innlogget bruker (lege). DIPS proprietært?
```json
{
    "resourceType": "Bundle",
    "type": "searchset",
    "total": 1,
    "entry": [
        {
            "fullUrl": "https://vt-sb-srv.dips.no/DIPS-WebAPI/HL7/FHIR-R4/PractitionerRole/agb1004491",
            "resource": {
                "resourceType": "PractitionerRole",
                "id": "agb1004491",
                "meta": {
                    "lastUpdated": "2024-04-09T14:13:30+02:00",
                    "profile": [
                        "DIPSPractitionerRole",
                        "NoBasisPractitionerRole"
                    ],
                    "tag": [
                        {
                            "system": "http://dips.no/fhir/namingsystem/practitionerrolesource",
                            "code": "practitionerRole"
                        }
                    ]
                },
                "contained": [
                    {
                        "resourceType": "Practitioner",
                        "identifier": [
                            {
                                "use": "official",
                                "system": "urn:oid:2.16.578.1.12.4.1.4.4",
                                "value": "357908642"
                            }
                        ],
                        "name": [
                            {
                                "family": "NAV",
                                "given": [
                                    "ERIK"
                                ]
                            }
                        ]
                    }
                ],
                "extension": [
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleHealthCarePartyType",
                        "valueString": "Person"
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationType",
                        "valueCodeableConcept": {
                            "coding": [
                                {
                                    "extension": [
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationProtocol",
                                            "valueCoding": {
                                                "system": "http://dips.no/fhir/namingsystem/communication-protocol",
                                                "code": "ARBFLYT",
                                                "display": "Dokument til signering i DIPS Arbeidsflyt"
                                            }
                                        },
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationTypeId",
                                            "valueString": "110700"
                                        }
                                    ],
                                    "system": "http://dips.no/fhir/namingsystem/communication-type",
                                    "code": "EP",
                                    "display": "Epikrise"
                                },
                                {
                                    "extension": [
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationProtocol",
                                            "valueCoding": {
                                                "system": "http://dips.no/fhir/namingsystem/communication-protocol",
                                                "code": "RTGXML",
                                                "display": "KITH XML 1.2  Svarmelding (EDI Broker)"
                                            }
                                        },
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationTypeId",
                                            "valueString": "110701"
                                        },
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleIsPaperCopy",
                                            "valueDecimal": 1
                                        }
                                    ],
                                    "system": "http://dips.no/fhir/namingsystem/communication-type",
                                    "code": "RTG",
                                    "display": "Røntgensvar"
                                },
                                {
                                    "extension": [
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationProtocol",
                                            "valueCoding": {
                                                "system": "http://dips.no/fhir/namingsystem/communication-protocol",
                                                "code": "XMLMSBRO",
                                                "display": "KITH XML (MessageBroker)"
                                            }
                                        },
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationTypeId",
                                            "valueString": "224536"
                                        }
                                    ],
                                    "system": "http://dips.no/fhir/namingsystem/communication-type",
                                    "code": "RTGHV",
                                    "display": "Røntgenhenvisning"
                                },
                                {
                                    "extension": [
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationProtocol",
                                            "valueCoding": {
                                                "system": "http://dips.no/fhir/namingsystem/communication-protocol",
                                                "code": "XMLKITHHV",
                                                "display": "KITH Henvisning XML versjon 1.0"
                                            }
                                        },
                                        {
                                            "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleCommunicationTypeId",
                                            "valueString": "262135"
                                        }
                                    ],
                                    "system": "http://dips.no/fhir/namingsystem/communication-type",
                                    "code": "HENV",
                                    "display": "Henvisning"
                                }
                            ]
                        }
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleHealthcarePartyDepartment",
                        "valueReference": {
                            "reference": "Organization/afa22",
                            "identifier": {
                                "use": "official",
                                "system": "urn:oid:1.3.6.1.4.1.9038.70.3",
                                "value": "22"
                            }
                        }
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleHospital",
                        "valueReference": {
                            "reference": "Organization/afm1",
                            "identifier": {
                                "use": "official",
                                "system": "urn:oid:2.16.578.1.12.4.1.4.101",
                                "value": "970948139"
                            }
                        }
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleUserRoleDepartment",
                        "valueReference": {
                            "reference": "Organization/afa22",
                            "identifier": {
                                "use": "official",
                                "system": "urn:oid:1.3.6.1.4.1.9038.70.3",
                                "value": "22"
                            }
                        }
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleDipsSignature",
                        "valueString": "NAV-ERIK"
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleUserRoleLastUpdated",
                        "valueDateTime": "2024-03-21T13:22:21+00:00"
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleUserRoleName",
                        "valueString": "NAV-ERIK Full funksjonstilgang og VID datatilgang (BT)"
                    },
                    {
                        "url": "http://dips.no/fhir/StructureDefinition/R4/DIPSPractitionerRoleUserRoleId",
                        "valueString": "1010248"
                    }
                ],
                "identifier": [
                    {
                        "use": "official",
                        "system": "urn:oid:1.3.6.1.4.1.9038.51",
                        "value": "NAV-ERIK"
                    },
                    {
                        "use": "official",
                        "system": "urn:oid:1.3.6.1.4.1.9038.51.1",
                        "value": "1004491"
                    },
                    {
                        "use": "official",
                        "system": "urn:oid:2.16.578.1.12.4.1.4.4",
                        "value": "357908642"
                    }
                ],
                "active": true,
                "practitioner": {
                    "reference": "Practitioner/stf2018663",
                    "identifier": {
                        "use": "official",
                        "system": "urn:oid:2.16.578.1.12.4.1.4.4",
                        "value": "357908642"
                    }
                },
                "organization": {
                    "reference": "Organization/aks1",
                    "identifier": {
                        "use": "official",
                        "system": "urn:oid:2.16.578.1.12.4.1.4.101",
                        "value": "970948139"
                    },
                    "display": "Testsykehuset HF"
                },
                "code": [
                    {
                        "coding": [
                            {
                                "system": "urn:oid:1.3.6.1.4.1.9038.52.1012",
                                "code": "1"
                            },
                            {
                                "system": "http://terminology.hl7.org/CodeSystem/practitioner-role",
                                "code": "1",
                                "display": "Doctor"
                            }
                        ],
                        "text": "Avdelingsoverlege"
                    }
                ],
                "telecom": [
                    {
                        "system": "phone",
                        "value": "75505000",
                        "use": "work"
                    }
                ]
            },
            "search": {
                "mode": "match"
            }
        }
    ]
}
```

## Organization.GET
```json
{
    "resourceType": "Organization",
    "id": "aks1",
    "meta": {
        "profile": [
            "DIPSOrganization",
            "NoBasisOrganization"
        ],
        "security": [
            {
                "system": "http://dips.no/fhir/InternalSecurityAccess",
                "code": "A",
                "display": "ALL"
            }
        ],
        "tag": [
            {
                "system": "http://dips.no/fhir/namingsystem/organizationsource",
                "code": "organization"
            }
        ]
    },
    "text": {
        "div": "<table><tr><td>Name</td><td>Testsykehuset Hf</td></tr><tr><td>Address</td><td><table><tr><td><table><tr><td>Type</td><td>Physical</td></tr><tr><td>Line</td><td><table><tr><td>Testveien 10</td></tr></table></td></tr><tr><td>City</td><td>Bodø</td></tr><tr><td>PostalCode</td><td>8015</td></tr></table></td></tr><tr><td><table><tr><td>Type</td><td>Postal</td></tr><tr><td>Line</td><td><table><tr><td>Legeveien 22</td></tr></table></td></tr><tr><td>City</td><td>Bodø</td></tr><tr><td>PostalCode</td><td>8009</td></tr></table></td></tr></table></td></tr><tr><td>Id</td><td>aks1</td></tr></table>"
    },
    "extension": [
        {
            "url": "http://DIPS.no/fhir/StructureDefinition/R4/Organization-bankAccountNumber1",
            "valueString": "1 234 567001"
        },
        {
            "url": "http://DIPS.no/fhir/StructureDefinition/R4/Organization-bankAccountNumber2",
            "valueString": "1234567"
        }
    ],
    "identifier": [
        {
            "use": "official",
            "system": "urn:oid:1.3.6.1.4.1.9038.70.1",
            "value": "1"
        },
        {
            "use": "official",
            "system": "urn:oid:2.16.578.1.12.4.1.4.101",
            "value": "970948139"
        },
        {
            "use": "official",
            "system": "urn:oid:2.16.578.1.12.4.1.2",
            "value": "79744"
        }
    ],
    "active": true,
    "type": [
        {
            "coding": [
                {
                    "system": "urn:oid:2.16.578.1.12.4.1.1.8628",
                    "code": "2",
                    "display": "HF|Helseforetak"
                },
                {
                    "extension": [
                        {
                            "url": "http://DIPS.no/fhir/StructureDefinition/R4/OrganizationTypeCodeId",
                            "valueIdentifier": {
                                "use": "official",
                                "system": "http://dips.no/fhir/namingsystem/dips-organizationtypecodeid",
                                "value": "100310"
                            }
                        }
                    ],
                    "system": "http://dips.no/fhir/namingsystem/dips-organizationtype",
                    "display": "Helseforetak"
                }
            ],
            "text": "Helseforetak"
        }
    ],
    "name": "Testsykehuset Hf",
    "telecom": [
        {
            "system": "phone",
            "value": "75505000",
            "use": "work"
        }
    ],
    "address": [
        {
            "extension": [
                {
                    "url": "http://DIPS.no/fhir/StructureDefinition/R4/Organization-addressId",
                    "valueIdentifier": {
                        "use": "official",
                        "system": "http://dips.no/fhir/namingsystem/dips-addressid",
                        "value": "1"
                    }
                },
                {
                    "url": "http://hl7.no/fhir/StructureDefinition/R4/no-basis-propertyinformation",
                    "valueCoding": {
                        "system": "urn:oid:2.16.578.1.12.4.1.1.3402",
                        "code": "1804",
                        "display": "BODØ"
                    }
                }
            ],
            "use": "work",
            "type": "physical",
            "line": [
                "Testveien 10"
            ],
            "city": "Bodø",
            "district": "BODØ",
            "state": "NORDLAND FYLKESKOMMUNE",
            "postalCode": "8015"
        },
        {
            "extension": [
                {
                    "url": "http://DIPS.no/fhir/StructureDefinition/R4/Organization-addressId",
                    "valueIdentifier": {
                        "use": "official",
                        "system": "http://dips.no/fhir/namingsystem/dips-addressid",
                        "value": "2"
                    }
                }
            ],
            "use": "billing",
            "type": "postal",
            "line": [
                "Legeveien 22"
            ],
            "city": "Bodø",
            "postalCode": "8009"
        }
    ],
    "partOf": {
        "reference": "Organization/aks1000004",
        "identifier": {
            "use": "official",
            "system": "urn:oid:2.16.578.1.12.4.1.4.101",
            "value": "970948100"
        },
        "display": "Helse Nord"
    }
}
```

## DocumentReference.POST
Benyttes for å lagre utfylt legeerklæring (PDF) i EPJ
