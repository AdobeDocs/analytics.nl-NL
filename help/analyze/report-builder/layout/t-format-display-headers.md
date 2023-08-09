---
description: Leer hoe te om uw rapport te noemen en te vormen hoe te om rij en kolomkopballen te tonen.
title: Weergavekoppen opmaken
uuid: cd0e167b-9463-43fd-87b2-724d1c79de68
feature: Report Builder
role: User, Admin
exl-id: 168daa6b-965c-4f8b-97b7-651a7ad55d6c
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 2%

---

# Weergavekoppen opmaken

U kunt uw rapport noemen en vormen hoe te om rij en kolomkopballen te tonen. De koppeling Opmaakopties is beschikbaar voor de typen Draaien en Aangepaste layout.

1. Maak een aanvraag op het tabblad [!UICONTROL Request Wizard: Step 1].
1. Klik op **[!UICONTROL Next]**.
1. Op de [!UICONTROL Request Wizard: Step 2] formulier, voegt u de gewenste afmetingen en metrische gegevens toe aan de aanvraag.
1. Klik op **[!UICONTROL Format Options]**.
1. Vorm [!UICONTROL Display] opties:

   | Element | Beschrijving |
   |--- |--- |
   | Rapportnaam | Toont of de naam van het rapporttype u van de boom in de Tovenaar van het Verzoek selecteerde: Stap 1 (bijvoorbeeld, [!DNL Traffic Report]) of de naam die u in het dialoogvenster [!DNL Name this Request] veld. |
   | Filterparameters | Geeft de dimensiefilters weer, zoals een zoekfilter. |
   | Segment | Toont de segmentparameter. |
   | Recente gegevens | Hiermee geeft u parameters voor gegevensrecentie weer. Bijvoorbeeld: Gegevensrecentie: paginaweergaven (1,5 uur geleden), Afsluiten (30 minuten geleden) Zie [Opties](/help/analyze/report-builder/options.md) voor informatie over de huidige gegevensverwerking. |

   Met betrekking tot de weergavevolgorde, als de [!UICONTROL Row Label] het net (op Stap 2) bevat een punt, het eerst in het verzoek wordt getoond. Als dat niet het geval is, gebruikt het systeem het eerste item in de [!UICONTROL Column Label] raster. Als er geen rij- of kolomitems bestaan, wordt het eerste item in het dialoogvenster [!UICONTROL Metrics] raster wordt weergegeven.

   **Rij- en kolomkoppen weergeven:** Hiermee voegt u een rij en kolom toe om deze items weer te geven.

   In versie 3.11 kunt u een koptekst voor elk item weergeven. Versie 4 toont al deze punten of geen van hen. Als u een verzoek in versie 3.11 creeerde en het in versie 4.x opent, vraagt de rapportbouwer u in Stap 2 om de waaier voor punten bij te werken die een kopbal missen.

   **Kopteksten wijzigen in automatisch te filteren Excel-bestanden:** Alleen beschikbaar als rij- en kolomkoppen worden weergegeven. Dit het plaatsen leidt tot een autofilter van Excel en voegt het aan de bouwer van het gegevensrapport voor dit verzoek toe.

   >[!NOTE]
   >
   >Excel ondersteunt slechts één automatisch filter per werkblad. Als u een nieuw automatisch filter maakt in een werkblad waar al een automatisch filter aanwezig is, geeft Excel geen waarschuwing dat het bestaande automatische filter wordt vervangen.

   **Automatisch omtrekken uitvoeren:** Transformeert de datum die door rapportaannemer van een lijstmening aan een boomstructuurmening is teruggekeerd.

   **Geef deze aanvraag een naam:** Hiermee kunt u een door de gebruiker gedefinieerde naam voor de aanvraag typen of de standaardnaam gebruiken die is geselecteerd in Stap 1. Deze naam verschijnt als [!UICONTROL Report] naam in de [!UICONTROL Request Manager]. Zie [Een aanvraag een naam geven](/help/analyze/report-builder/layout/name-a-request.md).

1. Klik op **[!UICONTROL OK]**.
