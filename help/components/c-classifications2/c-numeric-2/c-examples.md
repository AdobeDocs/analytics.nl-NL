---
description: Voorbeelden voor het importeren van numerieke 2-classificaties.
subtopic: Classifications
title: Voorbeelden
topic: Admin tools
uuid: 0553d07f-87c1-4372-90ce-7118a6393a01
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Voorbeelden

Voorbeelden voor het importeren van numerieke 2-classificaties.

<!-- 

c_example_1__rate.xml

 -->

In dit geval hebt u de classificatie gemaakt voor de [!UICONTROL Classification Conversion] manager en wilt u de waarden voor januari importeren:

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_jan_var` |  | `.2` |
| Product2 | Text2 | `Cost2_jan_var` |  | `.3` |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 - 2010/01/31 | inkomsten | inkomsten |
| 2010/01/01 - 2010/01/31 | inkomsten | inkomsten |

In januari had Product1 een kostprijs van 20% van zijn inkomsten (weergegeven in `~MyCost^~value~`) en Product2 had 30% van zijn inkomsten. Omdat u een nieuwe rij importeert, `~MyCost^~id~` is deze leeg.

## Resultaat {#section_E0569289C9B34C479C7D2CD9ECBF866E}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: jan. 2010

Rapport: Producten

| Producten | Ontvangsten | MijnKosten |
|---|---|---|
| Product1 | $10,000.23 | $2000.05 |
| Product2 | $9,000.04 | $2700.01 |

<!-- 

c_example_2__rate.xml

 -->

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_jan_var` | 1 | .2 |
| Product2 | Text2 | `Cost2_jan_var` | 2 | .3 |
| Product1 | Text1 | `Cost1_feb_var` |  | .15 |
| Product2 | Text2 | `Cost2_feb_var` |  | .25 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 - 2010/01/31 | inkomsten | inkomsten |
| 2010/01/01 - 2010/01/31 | inkomsten | inkomsten |
| 2010/02/01 - 2010/02/28 | inkomsten | inkomsten |
| 2010/02/01 - 2010/02/28 | inkomsten | inkomsten |

In februari daalden de kosten van de gebruiker voor Product1 tot 15% van de opbrengst, en Product2 daalde tot 25% van zijn opbrengst.

## Resultaat {#section_23DF5353AC1B478C88647F222703352C}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: jan. 2010

Rapport: Producten

| Producten | Ontvangsten | MijnKosten |
|---|---|---|
| Product1 | $10,000.23 | $2000.05 |
| Product2 | $9,000.04 | $2700.01 |

Periode: feb. 2010

Rapport: Producten

| Producten | Ontvangsten | MijnKosten |
|---|---|---|
| Product1 | $15,500.75 | $2325.11 |
| Product2 | $12,300.52 | $3075.13 |

Periode: 1 jan. 2010 - 28 feb. 2010

Rapport: Producten

| Producten | Ontvangsten | MijnKosten |
|---|---|---|
| Product1 | $25,500.98 | $4325.16 |
| Product2 | $21,300.56 | $5,775.14 |

<!-- 

c_example_3__fixed.xml

 -->

Daarom importeert u de volgende gegevens:

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_fixed` |  | 3000.00 |
| Product2 | Text2 | `Cost2_jan_fixed` |  | 2000.00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | vast | none |
| 2010/03/01 - 2010/03/31 | vast | none |

## Resultaat {#section_674B57ADB8284B878F9E670038C31464}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: mrt. 2010

Rapport: Producten

| Producten | Ontvangsten | MijnKosten |
|---|---|---|
| Product1 | $11,023.75 | $3000.00 |
| Product2 | $8,000.12 | $2000.00 |

<!-- 

c_example_4__(advanced)_multiple_row_per_time_period.xml

 -->

In dit voorbeeld voegt u een verzendkosten van 500 euro toe aan Product1 voor januari en een verzendkosten van 600 euro aan februari.

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_jan_var` | 1 | .2 |
| Product1 | Text1 | `Cost2_jan_fixed` |  | 500 |
| Product1 | Text1 | `Cost1_feb_var` | 2 | .15 |
| Product1 | Text1 | `Cost2_feb_fixed` |  | 600 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/01/01 - 2010/01/31 | inkomsten | inkomsten |
| 2010/01/01 - 2010/01/31 | vast | none |
| 2010/02/01 - 2010/01/31 | inkomsten | inkomsten |
| 2010/02/01 - 2010/01/31 | vast | none |

De rijen die eerder werden ingevoerd hebben een identiteitskaart, die erop wijst dat zij geen nieuwe kosten zijn.

## Resultaat {#section_2096084176614B9AA60F97D5853CB9EA}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: jan. 2010

Rapport: Producten

| Producten | Ontvangsten | MijnKosten |
|---|---|---|
| Product1 | $10,000.23 | $2500.05 |

> [!NOTE] Geavanceerde gebruikers kunnen deze functie gebruiken om de waarden te benaderen. De resulterende informatie mag niet worden behandeld als exacte waarden.

<!-- 

c_example_5__identical_rate_hinge.xml

 -->

In het volgende voorbeeld wordt dit getoond:

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_var` |  | 1 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | bestellen | bestellen |

## Resultaat {#section_39E24ECCC3B34C9AADC25572662750E5}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: mrt. 2010

Rapport: Producten op pagina

| Producten op pagina | Orders | MijnKosten |
|---|---|---|
| Product1 | 1000 | $1000.00 |
| Startpagina | 600 | $600 |
| Winkelwagentje | 400 | $400 |

<!-- 

c_example_5__fixed_no_hinge.xml

 -->

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_fixed` |  | 3000.00 |
| Product2 | Text2 | `Cost2_mar_fixed` |  | 2000.00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | vast | none |
| 2010/03/01 - 2010/03/31 | vast | none |

## Resultaat {#section_7F5F5970077D4E14A5DC91495E23540D}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: mrt. 2010

Rapport: Producten op pagina

| Producten op pagina | Orders | MijnKosten |
|---|---|---|
| Product1 | 1000 | $3000.00 |
| Startpagina | 600 | 0 |
| Winkelwagentje | 400 | 0 |

<!-- 

c_example_7__fixed_hinge.xml

 -->

In dit geval importeert u de volgende gegevens:

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | `Cost1_mar_fixed` |  | 3000.00 |
| Product2 | Text2 | `Cost2_mar_fixed` |  | 2000.00 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | vast | inkomsten |
| 2010/03/01 - 2010/03/31 | vast | inkomsten |

## Resultaat {#section_5953BB6FD0CE4EF69D1D60B8B1203431}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: mrt. 2010

Rapport: Producten op pagina

| Producten op pagina | Orders | MijnKosten |
|---|---|---|
| Product1 | 1000 | $3000.00 |
| Startpagina | 600 | $1800.00 |
| Winkelwagentje | 400 | $1200.00 |

<!-- 

c_example_7_continued__different_rate_hinge.xml

 -->

In dit geval importeert u de volgende bestandsgegevens:

| Sleutel | MyText | `~MyCost` | `~MyCost^~id~` | `~MyCost^~value~` |
|---|---|---|---|---|
| Product1 | Text1 | Kosten1_mar_fixed |  | 3 |

| `~MyCost^~period~` | `~MyCost^~rate~` | `~MyCost^~hinge~` |
|---|---|---|
| 2010/03/01 - 2010/03/31 | bestellen | inkomsten |

## Resultaat {#section_6E2604D9A3B0455585EFF0F80FF54127}

Een voorbeeld van output van het rapport wordt hier getoond:

Periode: mrt. 2010

Rapport: Producten op pagina

| Producten op pagina | Orders | MijnKosten |
|---|---|---|
| Product1 | 1000 | $3000.00 |
| Startpagina | 600 | $1,000.00 |
| Winkelwagentje | 400 | $2,000.00 |

