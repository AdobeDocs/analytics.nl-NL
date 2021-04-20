---
description: Voorbeelden, notities en syntaxisnotities over het gebruik van datumbereiken in aangepaste expressies.
title: Voorbeelden van datumbereiken met aangepaste expressies
uuid: 3f46816d-9eee-4b2d-83be-bf1c9fb97fcf
feature: Report Builder
role: Business Practitioner, Administrator
translation-type: tm+mt
source-git-commit: 894ee7a8f761f7aa2590e06708be82e7ecfa3f6d
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 5%

---


# Voorbeelden van datumbereiken met aangepaste expressies

Voorbeelden, notities en syntaxisnotities over het gebruik van datumbereiken in aangepaste expressies.

De tabel gaat ervan uit dat de datum van vandaag maandag 10 november 2011 is, met de Gregoriaanse kalender.

| Voorbeeld | Datumbereik | Expressie aanpassen | Datum Bereik rapport |
|---|---|---|---|
|  |  | **Van** | **Naar** |  |
| 3 | Twee weken geleden | cw-2w | cw-1w-1d | 26 okt tot 1 nov. |
| 2 | Eerste drie dagen van de vijfde maand van het afgelopen jaar | cy-1y+4m | cy-1y+4m+2d | 1 mei tot en met 3 mei 2010 |
| 3 | Een volledige week, vanaf 4 weken geleden | cw-4w | cw-3w-1d | 12 okt tot en met 18 okt. |
| 4 | Vorige week in het voorgaande jaar | cw-53w | cw-52w-1d | nov. t/m 9 nov. 2010 |
| 5 | Een maand die twee maanden geleden begint | cm-2m | cm-1m-1d | 1 sep. t/m 30 sep. |
| 6 | 12 maanden geleden in het voorgaande jaar | cm-12 m | cm-11m-1d | 1 nov. t/m 30 nov. 2010 |

## Opmerkingen over voorbeelden {#section_37801B0D6D364ABAA8DCE3A4C0123B2C}

**Voorbeeld 1**

Als vandaag maandag, 10 november 2011 is, neem de huidige datum en trek één week af om de laatste volledige week van oktober te verkrijgen.

**Voorbeeld 2**

Voeg vier maanden toe aan het begin van het jaar (de maand januari) om de maand mei te krijgen; Voeg twee dagen toe aan de eerste dag van de maand om de derde dag van de maand te krijgen.

## Syntaxisnotities {#section_555D6563B2D94FA3BDD801DC0B8C289D}

Aangepaste expressies die de meeste datumbereiken beslaan, kunnen worden gemaakt door twee termen aan een operator te koppelen. Een term is een combinatie van een geheel getal vermenigvuldiger en een punt afkorting. Een voorbeeld van een term is 18d. Een voorbeeld van een operator is +.

* Spaties tussen operatoren en termen zijn niet toegestaan.
* Gebruik alleen deze afkortingen: cd cw cm cq cy d w m q y
* De beste manier is om dezelfde datumreferentie te gebruiken in de begindatum en de einddatum: cd, cd of cw, cw of cy, cy. Het mengen van datumverwijzingen kan tot ongeldige data op bepaalde tijden van het jaar leiden.
* Geldige veelvouden van de afkortingen d w m q y worden gevormd door gehele getallen ( 1 2 3 ... ) toegevoegd aan de afkorting, bijvoorbeeld 53d 3w 5q 9m 2y
* Getallen zonder gehele getallen zijn niet toegestaan.
* De afkorting mag niet met een nul worden voorgevuld. 0w is bijvoorbeeld niet toegestaan.
* De volgende operatoren worden gebruikt om afkortingen samen te voegen: + -
* Omdat datumbereiken moeten worden herkend ten opzichte van de huidige periode, begint de eerste term in een expressie altijd met c.

