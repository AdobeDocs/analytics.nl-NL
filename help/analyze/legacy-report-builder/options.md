---
description: Meer informatie over de opties voor Report Builder.
title: Opties voor Report Builder
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
feature: Report Builder
role: User, Admin
exl-id: d3388990-7919-461d-a96e-4c996b8bdb8b
source-git-commit: 12d048b42c6a61e03dbbe73acb9d34df3e37693c
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Report Builder-opties

In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.

1. Klik op de werkbalk Add-ins op **[!UICONTROL Options]** ![ ](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg) :

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL As Of Date] |  |
| Instellen op huidige datum | Hiermee kunt u de [!UICONTROL As Of Date] opgeven of opnieuw instellen, zodat de Report Builder de huidige datum gebruikt of u wordt gevraagd welke datum moet worden gebruikt bij het vernieuwen. |
| Mij vragen om in te stellen bij vernieuwen | Hiermee kunt u de [!UICONTROL As Of Date] instellen wanneer u een aanvraag vernieuwt. |
| [!UICONTROL Data Recency] |  |
| [!UICONTROL Include Current Data] | Hiermee kunt u de latentie van gegevens (ook wel [!UICONTROL Data Recency] genoemd) tot de minuut in rapportage weergeven, soms zelfs voordat deze gegevens door Adobe Analytics zijn verwerkt.<br> wanneer u deze optie niet gebruikt, wordt de gefinaliseerde (verwerkte) wijze gebruikt, die typisch meer [ latent ](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html) is.<br> dit het plaatsen is op alle verzoeken in het werkboek van toepassing die verenigbare Huidige Gegevens zijn. Als het verzoek niet compatibel is, wordt de voltooide modus toegepast.<br> neem nota van de volgende situaties om de [!UICONTROL Include Current Data] wijze te gebruiken:<br>**Opties van het Formaat**: U kunt specificeren of om deze informatie ([!UICONTROL Data Recency]) te tonen wanneer [ het formatteren vertoningskopballen ](/help/analyze/legacy-report-builder/layout/t-format-display-headers.md).<br>**Ontbrekingen**: Niet gesteund. Als de [!UICONTROL Data Recency] -modus is ingesteld op Huidige gegevens en een van de aanvragen een onderverdeeld element bevat, wordt de niet-huidige gegevensmodus hersteld. Andere verzoeken, echter, blijven de Huidige wijze van Gegevens gebruiken.<br>**Manager van het Verzoek**: U kunt een Huidige kolom van Gegevens in de Manager van het Verzoek bekijken, zodat u kunt zien of wordt het plaatsen toegepast op een gepland verzoek.<br>**Geplande Werkboeken**: Deze wijze wordt opgeslagen tijdens het plannen proces op het werkboekniveau. Als u een gepland werkboek opent dat gefinaliseerde gegevens gebruikt, en [!UICONTROL Include Current Data] toepast, wordt de huidige wijze daarna gebruikt.<br>**Toestemmingen**: Voor gebruikers die geen toegang tot huidige gegevens hebben, is deze optie verborgen.  Als u deze optie inschakelt en een of meer verzoeken niet kunnen worden toegepast, wordt een waarschuwing weergegeven. |
| Waarschuwingen met betrekking tot verzoeken die niet compatibel zijn met huidige gegevens uitschakelen | Hiermee geeft u waarschuwingen weer als de modus [!UICONTROL Include Current Data] is geselecteerd, maar de gegevensmodus niet kan worden toegepast op de bewerkte aanvraag.  Als u bijvoorbeeld [!UICONTROL Include Current Data] instelt en vervolgens een aanvraag bewerkt waarvoor een segment is geselecteerd, wordt een waarschuwing weergegeven. |
| Aanvragen voor Report Builder van logbestanden naar lokaal bestand (voor probleemoplossing) | Hiermee kunt u aanvragen bij een lokaal bestand aanmelden. Gebruik dit logbestand voor probleemoplossing. |
| Getypte waarde interpreteren... | Interpreteert een getypte waarde in een filtercontrole als celplaats alvorens het een filteruitdrukking te overwegen.<br> bijvoorbeeld als u Hoogste 10 verzoek van de Pagina creeert, gebruikend een filterschoenen, zou het verzoek een cel tonen die iets gelijkend op bevat:   Filter: eerste tot tien pagina&#39;s, pagina bevat presentaties |
| Bijwerken wanneer een nieuwe versie beschikbaar is | Geeft aan het systeem door dat u op de hoogte wordt gesteld als er een nieuwe versie beschikbaar is voor de installatie. |
