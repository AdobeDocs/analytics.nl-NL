---
description: In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.
title: Opties van de functie Report Builder
topic: Report builder
uuid: f2920dee-4245-4617-a02e-03726dde2bb5
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Opties van de functie Report Builder

In het deelvenster Opties kunt u de datuminstellingen, latentie-instellingen (Huidige gegevens), loggegevens en updates configureren.

1. Klik op de werkbalk Add-ins op **[!UICONTROL Options]**![](assets/options_icon.png):

| Element | Beschrijving |
|--- |--- |
| [!UICONTROL As Of Date] |  |
| Instellen op huidige datum | Hier kunt u de huidige datum opgeven of opnieuw instellen, [!UICONTROL As Of Date] zodat de rapportbuilder de huidige datum gebruikt of u wordt gevraagd welke datum u na het vernieuwen moet gebruiken. |
| Mij vragen om in te stellen bij vernieuwen | Hiermee kunt u de instelling instellen [!UICONTROL As Of Date] bij het vernieuwen van een aanvraag. |
| [!UICONTROL Data Recency] |  |
| [!UICONTROL Include Current Data] | Hiermee kunt u de latentie van gegevens (ook wel [!UICONTROL Data Recency]) tot op het moment van rapportage bekijken, soms zelfs voordat deze gegevens door Adobe Analytics zijn verwerkt.<br>Wanneer u deze optie niet gebruikt, wordt de voltooide modus (verwerkt) gebruikt, die doorgaans [latent](https://marketing.adobe.com/resources/help/en_US/reference/data_latency.html)is.<br>Dit het plaatsen is op alle verzoeken in het werkboek van toepassing die verenigbare Huidige Gegevens zijn. Als het verzoek niet compatibel is, wordt de voltooide modus toegepast.<br>Houd u aan de volgende situaties voor het gebruik van de [!UICONTROL Include Current Data] modus:<br>**Opmaakopties **: U kunt opgeven of deze informatie ([!UICONTROL Data Recency]) moet worden weergegeven bij het[opmaken van weergavekoppen](/help/analyze/report-builder/layout/t-format-display-headers.md).<br>**Uitsplitsingen**: Niet ondersteund. Als de [!UICONTROL Data Recency] wijze aan de Huidige Gegevens wordt geplaatst, en één van de verzoeken een onderbreking element bevat, keert dit verzoek aan huidig gegevenswijze terug. Andere verzoeken, echter, blijven de Huidige wijze van Gegevens gebruiken.<br>**Aanvraagbeheer **: U kunt een kolom Huidige gegevens weergeven in Request Manager, zodat u kunt zien of de instelling wordt toegepast op een geplande aanvraag.<br>**Geplande werkboeken**: Deze wijze wordt opgeslagen tijdens het het plannen proces op het werkboekniveau. Als u een gepland werkboek opent dat gefinaliseerde gegevens gebruikt, en [!UICONTROL Include Current Data]toepast, wordt de huidige wijze gebruikt daarna.<br>**Machtigingen **: Deze optie is verborgen voor gebruikers die geen toegang hebben tot de huidige gegevens.  Als u deze optie inschakelt en een of meer verzoeken niet kunnen worden toegepast, wordt een waarschuwing weergegeven. |
| Waarschuwingen met betrekking tot verzoeken die niet compatibel zijn met huidige gegevens uitschakelen | Hiermee geeft u waarschuwingen weer als de [!UICONTROL Include Current Data] modus is geselecteerd, maar de gegevensmodus niet kan worden toegepast op de bewerkte aanvraag.  Als u bijvoorbeeld een aanvraag instelt [!UICONTROL Include Current Data]en vervolgens een aanvraag bewerkt waarvoor een segment is geselecteerd, wordt een waarschuwing weergegeven. |
| Aanvragen voor logboekrapportbuilder naar lokaal bestand (voor probleemoplossing) | Hiermee kunt u aanvragen bij een lokaal bestand aanmelden. Gebruik dit logbestand voor probleemoplossing. |
| Getypte waarde interpreteren... | Interpreteert een getypte waarde in een filtercontrole als celplaats alvorens het een filteruitdrukking te overwegen.<br>Als u bijvoorbeeld een aanvraag voor Top 10 van pagina&#39;s maakt en filterschoenen gebruikt, wordt in de aanvraag een cel weergegeven die iets bevat dat vergelijkbaar is met:   Filter: Bovenste 1-10 pagina, pagina bevat presentaties |
| Bijwerken wanneer een nieuwe versie beschikbaar is | Geeft aan het systeem door dat u op de hoogte wordt gesteld als er een nieuwe versie beschikbaar is voor de installatie. |
