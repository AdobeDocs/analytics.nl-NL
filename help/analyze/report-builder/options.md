---
description: In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.
title: Report Builder-opties
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
feature: Report Builder
role: User, Admin
exl-id: d3388990-7919-461d-a96e-4c996b8bdb8b
source-git-commit: 602f837689186f232c4c0f8baebbcf911446bc99
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# Report Builder-opties

In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.

1. Klik op de werkbalk Add-ins op **[!UICONTROL Options]** ![](https://spectrum.adobe.com/static/icons/workflow_18/Smock_Settings_18_N.svg):

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL As Of Date] |  |
| Instellen op huidige datum | Hiermee kunt u de  [!UICONTROL As Of Date] zodat gebruikt de rapportbouwer de huidige datum of vraagt u welke datum om te gebruiken op verfrist zich. |
| Mij vragen om in te stellen bij vernieuwen | Hiermee kunt u de  [!UICONTROL As Of Date] wanneer u een aanvraag vernieuwt. |
| [!UICONTROL Data Recency] |  |
| [!UICONTROL Include Current Data] | Hiermee kunt u gegevenslatentie weergeven (ook wel  [!UICONTROL Data Recency]) tot de minuut in rapportage, soms zelfs voordat deze gegevens door Adobe Analytics zijn verwerkt.<br>Wanneer u deze optie niet gebruikt, wordt de voltooide (verwerkte) wijze gebruikt, die typisch meer is [latent](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html).<br>Dit het plaatsen is op alle verzoeken in het werkboek van toepassing die verenigbare Huidige Gegevens zijn. Als het verzoek niet compatibel is, wordt de voltooide modus toegepast.<br>Let op de volgende situaties voor het gebruik van de [!UICONTROL Include Current Data] modus:<br>**Opmaakopties**: U kunt opgeven of deze informatie moet worden weergegeven ([!UICONTROL Data Recency]) wanneer [weergavekoppen opmaken](/help/analyze/report-builder/layout/t-format-display-headers.md).<br>**Uitsplitsingen**: Niet ondersteund. Als de  [!UICONTROL Data Recency] De modus wordt ingesteld op Huidige gegevens en een van de aanvragen bevat een onderverdelingen-element. Deze aanvraag wordt teruggezet naar de modus Niet-huidige gegevens. Andere verzoeken, echter, blijven de Huidige wijze van Gegevens gebruiken.<br>**Aanvraagbeheer**: U kunt een kolom Huidige gegevens weergeven in Request Manager, zodat u kunt zien of de instelling wordt toegepast op een geplande aanvraag.<br>**Geplande werkboeken**: Deze wijze wordt opgeslagen tijdens het het plannen proces op het werkboekniveau. Als u een gepland werkboek opent dat gefinaliseerde gegevens gebruikt, en van toepassing is [!UICONTROL Include Current Data], wordt de huidige modus daarna gebruikt.<br>**Machtigingen**: Deze optie is verborgen voor gebruikers die geen toegang hebben tot de huidige gegevens.  Als u deze optie inschakelt en een of meer verzoeken niet kunnen worden toegepast, wordt een waarschuwing weergegeven. |
| Waarschuwingen met betrekking tot verzoeken die niet compatibel zijn met huidige gegevens uitschakelen | Hiermee geeft u waarschuwingen weer als de  [!UICONTROL Include Current Data] wordt geselecteerd maar de gegevensmodus kan niet worden toegepast op de bewerkte aanvraag.  Als u bijvoorbeeld [!UICONTROL Include Current Data]en bewerk vervolgens een aanvraag waarvoor een segment is geselecteerd, wordt een waarschuwing weergegeven. |
| Aanvragen voor logboekrapportbuilder naar lokaal bestand (voor probleemoplossing) | Hiermee kunt u aanvragen bij een lokaal bestand aanmelden. Gebruik dit logbestand voor probleemoplossing. |
| Getypte waarde interpreteren... | Interpreteert een getypte waarde in een filtercontrole als celplaats alvorens het een filteruitdrukking te overwegen.<br>Als u bijvoorbeeld een aanvraag voor Top 10 van pagina&#39;s maakt en filterschoenen gebruikt, wordt in de aanvraag een cel weergegeven die iets bevat dat vergelijkbaar is met: Filter: Bovenste 1-10 pagina, pagina bevat presentaties |
| Bijwerken wanneer een nieuwe versie beschikbaar is | Geeft aan het systeem door dat u op de hoogte wordt gesteld als er een nieuwe versie beschikbaar is voor de installatie. |
