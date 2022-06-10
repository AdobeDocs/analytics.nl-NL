---
description: Waar de verwerkingsregels in de overkoepelende gegevenspijpleiding van Analytics verblijven.
subtopic: Processing rules
title: Verwerkingsvolgorde
feature: Processing Rules
exl-id: c7143527-017c-4550-b55e-09ea437d7c85
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 1%

---

# Verwerkingsvolgorde

Om de verwerkingsregels doeltreffend te kunnen gebruiken, is het van essentieel belang te begrijpen wanneer ze tijdens de gegevensverzameling worden toegepast.

![Verwerkingsvolgorde](assets/analytics_processing_order.png)

In de volgende tabellen worden de gegevens weergegeven die doorgaans beschikbaar zijn voordat en nadat de verwerkingsregels zijn toegepast.

## Voor het verwerken van regels

| Dimension | Beschrijving |
|--- |--- |
| [Dynamische variabelen](/help/implement/vars/page-vars/dynamic-variables.md) | Variabelen die dynamisch worden gevuld door informatie uit HTTP-headers of andere variabelen te halen. |
| [AppMeasurement](/help/implement/home.md) | Functies en insteekmodules die worden gebruikt in AppMeturement-bibliotheken, worden uitgevoerd in de browser of de clienttoepassing. |
| [Implementatie van tags](/help/implement/launch/overview.md) | Regels die zijn gedefinieerd in de Adobe Analytics-extensie in Adobe Experience Platform Data Collection. |
| [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/data-collection/adobe-analytics/analytics-overview.html) | Gegevens die via de SDK van het Web worden verzameld, worden naar Adobe Experience Edge verzonden en vervolgens naar de gewenste rapportsuite doorgestuurd. |
| [Bot-regels](/help/admin/admin/bot-removal/bot-rules.md) | Hiermee kunt u verkeer verwijderen dat wordt gegenereerd door bekende spinnen en bots. |

## Na verwerking regels

| Dimension | Beschrijving |
|--- |--- |
| Door VISTA toegevoegde gegevens | Verwerkingsregels worden toegepast vóór VISTA. |
| Bezoek het paginanummer | De verwerkingsregels zijn zich alleen bewust van de gegevens in de huidige hit. Het paginanummer van de bezoekpagina wordt gecompileerd nadat de verwerkingsregels worden toegepast. |
| Clean URL wordt toegevoegd als paginanaam als deze niet is ingesteld. | Nadat de verwerkingsregels en VISTA worden toegepast, wordt schone URL toegevoegd als paginanaam als er geen plaatste paginanaam is. Aangezien deze logica optreedt nadat de verwerkingsregels zijn toegepast, raadt Adobe aan een voorwaarde toe te voegen om te controleren of de paginanaam leeg is.  Als u de **[!UICONTROL Site Content]** > **[!UICONTROL Pages]** Rapport en u ziet URL-waarden voor paginanamen. De variabele paginanaam is waarschijnlijk leeg.  U kunt een voorwaarde instellen om te testen op een lege paginanaam of om te testen of de paginanaam of de pagina-URL een specifieke waarde bevat. De paginanaam kan vervolgens naar wens worden ingesteld. |
| Verwerkingsregels voor marketingkanalen | U kunt verwerkingsregels gebruiken om gegevens voor te bereiden voor verwerking door [Verwerkingsregels voor marketingkanalen](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-rules.html). |
| GEO-opzoekhandeling | Bevat de waarden voor de postcode van de bezoekerstaat en bezoeker. |
| Persistentie | Vars die zich in een vorige hit bevonden, blijven niet bij elke hit tijdens de regelverwerking behouden. Alleen eVars die zijn ingesteld op de huidige hit die wordt verwerkt, zijn beschikbaar. |

## Hoe de Regels van de Verwerking worden toegepast wanneer het kopiëren van Hits gebruikend VISTA

Als u een VISTA regel hebt die wordt gevormd om klappen aan een andere rapportreeks te kopiëren, worden de klappen verzonden door om het even welke verwerkingsregels die in de andere rapportreeks worden bepaald.

Als u verwerkingsregels hebt die op de originele rapportreeks worden bepaald, kunnen deze regels of niet worden toegepast gebaseerd op hoe de regel VISTA door de Diensten van de Techniek werd gevormd. Om te weten te komen, kunt u uw implementatiespecialist vragen of de VISTA-regel &quot;pre&quot;of &quot;post&quot;waarden aan de extra rapportreeks kopieert. Als de &quot;pre&quot;waarde wordt gekopieerd, worden de verwerkingsregels die op de originele rapportreeks worden bepaald niet toegepast. Als de &quot;post&quot;waarde wordt gekopieerd, worden de verwerkingsregels toegepast alvorens de slag wordt gekopieerd.
