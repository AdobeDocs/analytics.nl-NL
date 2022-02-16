---
description: Om de verwerkingsregels doeltreffend te kunnen gebruiken, is het van essentieel belang te begrijpen wanneer ze tijdens de gegevensverzameling worden toegepast.
subtopic: Processing rules
title: Verwerkingsvolgorde
feature: Processing Rules
exl-id: c7143527-017c-4550-b55e-09ea437d7c85
source-git-commit: 71b3b1937e7fa272f0497008e8e510204bbb4418
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# Verwerkingsvolgorde

Om de verwerkingsregels doeltreffend te kunnen gebruiken, is het van essentieel belang te begrijpen wanneer ze tijdens de gegevensverzameling worden toegepast.

![](assets/analytics_processing_order_test.png)

In de volgende tabellen worden de gegevens weergegeven die doorgaans beschikbaar zijn voordat en nadat de verwerkingsregels zijn toegepast:

## Voor het verwerken van regels

| Dimension | Beschrijving |
|--- |--- |
| Dynamische variabele zoekopdracht | Variabelen worden dynamisch gevuld door informatie uit HTTP-headers of andere variabelen te halen. Bijvoorbeeld: `s.eVar5="D=c1"` zal de waarde van prop1 in eVar5 zetten. |
| AppMeasurement | Functies en insteekmodules die in AppMeturement worden gebruikt, worden uitgevoerd in de browser of de clienttoepassing. |
| Tagbeheer | De regels die in UI van de Inzameling van Gegevens worden bepaald worden uitgevoerd zoals bepaald. |
| Bot-regels | [Bot-regels](/help/admin/admin/bot-removal/bot-rules.md) laat u verkeer verwijderen dat door bekende spinnen en bots uit uw rapportreeks wordt geproduceerd. |

## Na verwerking regels

| Dimension | Beschrijving |
|--- |--- |
| Door VISTA toegevoegde gegevens | Verwerkingsregels worden toegepast vóór VISTA. |
| Bezoek het paginanummer | Als algemene regel, zijn de verwerkingsregels zich bewust van de gegevens die in de huidige slechts treffer zijn. Het paginanummer van de bezoekpagina wordt gecompileerd nadat de verwerkingsregels worden toegepast. |
| Clean URL wordt toegevoegd als paginanaam als deze niet is ingesteld. | Nadat de verwerkingsregels en VISTA worden toegepast, wordt schone URL toegevoegd als paginanaam als er geen plaatste paginanaam is. Aangezien dit voorkomt nadat de verwerkingsregels worden toegepast, adviseren wij toevoegend een voorwaarde om te controleren als de paginanaam leeg is.  Als u Site Content > Pages Report uitvoert en u https://-waarden ziet voor paginanamen, is de paginanaam waarschijnlijk leeg en wordt de URL gebruikt.  U kunt een voorwaarde instellen om te testen op de naam van een lege pagina of om te testen of de paginanaam of de pagina-URL een specifieke waarde bevat. De paginanaam kan vervolgens naar wens worden ingesteld. |
| Verwerkingsregels voor marketingkanalen | U kunt verwerkingsregels gebruiken om gegevens voor te bereiden voor verwerking door [Verwerkingsregels voor marketingkanalen](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-rules.html). |
| GEO-opzoekhandeling | Hieronder vallen ook de waarden van de postcode voor de bezoekerstatus en de bezoeker. |
| Persistentie | Vars die zich in een vorige hit bevonden, blijven niet bij elke hit tijdens de regelverwerking behouden. Alleen eVars die zijn ingesteld op de huidige hit die wordt verwerkt, zijn beschikbaar. |

## Hoe de Regels van de Verwerking worden toegepast wanneer het kopiëren van Hits gebruikend VISTA {#section_576EE8C240A24CBA979BD614E8D5338D}

Als u een VISTA regel hebt die wordt gevormd om klappen aan een andere rapportreeks te kopiëren, worden de klappen verzonden door om het even welke verwerkingsregels die in de andere rapportreeks worden bepaald.

Als u verwerkingsregels hebt die op de originele rapportreeks worden bepaald, kunnen deze of niet worden toegepast gebaseerd op hoe de regel VISTA door de Diensten van de Techniek werd gevormd. Om te weten te komen, kunt u uw implementatiespecialist vragen of de VISTA-regel &quot;pre&quot;of &quot;post&quot;waarden aan de extra rapportreeks kopieert. Als de &quot;pre&quot;waarde wordt gekopieerd, worden de verwerkingsregels die op de originele rapportreeks worden bepaald niet toegepast. Als de &quot;post&quot;waarde wordt gekopieerd, worden de verwerkingsregels toegepast alvorens de slag wordt gekopieerd.
