---
description: In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.
title: Report Builder-opties
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
feature: Report Builder
role: Business Practitioner, Administrator
exl-id: d3388990-7919-461d-a96e-4c996b8bdb8b
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 2%

---

# Report Builder-opties

In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.

1. Klik op **[!UICONTROL Options]** ![](assets/options_icon.png) op de werkbalk Add-ins:

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL As Of Date] |  |
| Instellen op huidige datum | Hiermee kunt u de [!UICONTROL As Of Date] opgeven of opnieuw instellen, zodat de rapportbuilder de huidige datum gebruikt of u wordt gevraagd welke datum moet worden gebruikt bij vernieuwen. |
| Mij vragen om in te stellen bij vernieuwen | Hiermee kunt u de [!UICONTROL As Of Date] instellen wanneer u een verzoek vernieuwt. |
| [!UICONTROL Data Recency] |  |
| [!UICONTROL Include Current Data] | Hiermee kunt u de latentie van gegevens (ook wel [!UICONTROL Data Recency] genoemd) tot een minuut weergeven in rapportage, soms zelfs voordat deze gegevens door Adobe Analytics zijn verwerkt.<br>Wanneer u deze optie niet gebruikt, wordt de voltooide modus (verwerkt) gebruikt, die doorgaans  [latent](https://experienceleague.adobe.com/docs/analytics/analyze/reports-analytics/current-data.html) is.<br>Dit het plaatsen is op alle verzoeken in het werkboek van toepassing die verenigbare Huidige Gegevens zijn. Als het verzoek niet compatibel is, wordt de voltooide modus toegepast.<br>Houd u aan de volgende situaties voor het gebruik van de  [!UICONTROL Include Current Data] modus:<br>**Opmaakopties**: U kunt opgeven of deze informatie ([!UICONTROL Data Recency]) moet worden weergegeven bij het  [opmaken van weergavekoppen](/help/analyze/report-builder/layout/t-format-display-headers.md).<br>**Uitsplitsingen**: Niet ondersteund. Als de [!UICONTROL Data Recency] wijze aan de Huidige Gegevens wordt geplaatst, en één van de verzoeken een onderbreking element bevat, keert dit verzoek aan huidig gegevenswijze terug. Andere verzoeken, echter, blijven de Huidige wijze van Gegevens gebruiken.<br>**Aanvraagbeheer**: U kunt een kolom Huidige gegevens weergeven in Request Manager, zodat u kunt zien of de instelling wordt toegepast op een geplande aanvraag.<br>**Geplande werkboeken**: Deze wijze wordt opgeslagen tijdens het het plannen proces op het werkboekniveau. Als u een gepland werkboek opent dat gefinaliseerde gegevens gebruikt, en [!UICONTROL Include Current Data] toepast, wordt de huidige wijze daarna gebruikt.<br>**Machtigingen**: Deze optie is verborgen voor gebruikers die geen toegang hebben tot de huidige gegevens.  Als u deze optie inschakelt en een of meer verzoeken niet kunnen worden toegepast, wordt een waarschuwing weergegeven. |
| Waarschuwingen met betrekking tot verzoeken die niet compatibel zijn met huidige gegevens uitschakelen | Hiermee geeft u waarschuwingen weer als de modus [!UICONTROL Include Current Data] is geselecteerd, maar de gegevensmodus niet kan worden toegepast op de bewerkte aanvraag.  Bijvoorbeeld, als u [!UICONTROL Include Current Data] plaatst, en dan een verzoek uitgeeft dat een geselecteerd segment heeft, wordt een waarschuwing uitgegeven. |
| Aanvragen voor logboekrapportbuilder naar lokaal bestand (voor probleemoplossing) | Hiermee kunt u aanvragen bij een lokaal bestand aanmelden. Gebruik dit logbestand voor probleemoplossing. |
| Getypte waarde interpreteren... | Interpreteert een getypte waarde in een filtercontrole als celplaats alvorens het een filteruitdrukking te overwegen.<br>Als u bijvoorbeeld een aanvraag voor Top 10 van pagina&#39;s maakt en filterschoenen gebruikt, wordt in de aanvraag een cel weergegeven die iets bevat dat vergelijkbaar is met: Filter: Bovenste 1-10 pagina, pagina bevat presentaties |
| Bijwerken wanneer een nieuwe versie beschikbaar is | Geeft aan het systeem door dat u op de hoogte wordt gesteld als er een nieuwe versie beschikbaar is voor de installatie. |
