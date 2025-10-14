---
description: Leer hoe te om uw rapport te noemen en te vormen hoe te om rij en kolomkopballen te tonen.
title: Weergavekoppen opmaken
uuid: cd0e167b-9463-43fd-87b2-724d1c79de68
feature: Report Builder
role: User, Admin
exl-id: 168daa6b-965c-4f8b-97b7-651a7ad55d6c
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 1%

---

# Weergavekoppen opmaken

{{legacy-arb}}

U kunt uw rapport noemen en vormen hoe te om rij en kolomkopballen te tonen. De koppeling Opmaakopties is beschikbaar voor de typen Draaien en Aangepaste layout.

1. Maak een aanvraag op de [!UICONTROL Request Wizard: Step 1] .
1. Klik op **[!UICONTROL Next]**.
1. Voeg desgewenst afmetingen en cijfergegevens toe aan het verzoek in het [!UICONTROL Request Wizard: Step 2] -formulier.
1. Klik op **[!UICONTROL Format Options]**.
1. Configureer de opties voor [!UICONTROL Display] :

   | Element | Beschrijving |
   |--- |--- |
   | Rapportnaam | Geeft de naam weer van het rapporttype dat u hebt geselecteerd in de structuur in de wizard Verzoek: Stap 1 (bijvoorbeeld [!DNL Traffic Report] ) of de naam die u in het veld [!DNL Name this Request] typt. |
   | Filterparameters | Geeft de dimensiefilters weer, zoals een zoekfilter. |
   | Segment | Toont de segmentparameter. |
   | Recente gegevens | Hiermee geeft u parameters voor gegevensrecentie weer. Bijvoorbeeld:    Recentie van gegevens: De meningen van de pagina (1.5 uur geleden), uitgang (30 minuten geleden) zie [&#x200B; Opties &#x200B;](/help/analyze/legacy-report-builder/options.md) voor informatie over huidige gegevensverwerking. |

   Wat de weergavevolgorde betreft: als het raster [!UICONTROL Row Label] (bij Stap 2) een item bevat, wordt dit eerst in de aanvraag weergegeven. Als dat niet het geval is, gebruikt het systeem het eerste item in het [!UICONTROL Column Label] -raster. Als er geen rij- of kolomitems bestaan, wordt het eerste item in het [!UICONTROL Metrics] -raster weergegeven.

   **Kop van de Rij en van de Kolom van de Vertoning:** voegt een rij en een kolom toe om deze punten te tonen.

   In versie 3.11 kunt u een koptekst voor elk item weergeven. Versie 4 toont al deze punten of geen van hen. Als u een aanvraag hebt gemaakt in versie 3.11 en deze opent in versie 4.x, vraagt de Report Builder u in stap 2 om het bereik met één cel bij te werken voor items die een koptekst missen.

   **de Kopballen van de Verandering in de auto-Filters van Excel:** Beschikbaar slechts als de rij en de kolomkopballen worden getoond. Met deze instelling maakt u een automatisch Excel-filter en voegt u dit filter toe aan de geretourneerde gegevens voor deze Report Builder.

   >[!NOTE]
   >
   >Excel ondersteunt slechts één automatisch filter per werkblad. Als u een nieuw automatisch filter maakt in een werkblad waar al een automatisch filter aanwezig is, geeft Excel geen waarschuwing dat het bestaande automatische filter wordt vervangen.

   **voer auto-Overzicht uit:** zet de datum die door Report Builder van een lijstmening aan een boommening is teruggekeerd om.

   **Naam dit Verzoek:** laat u een user-defined naam voor het verzoek typen, of de standaardnaam gebruiken die op Stap 1 wordt geselecteerd. Deze naam wordt weergegeven als de naam [!UICONTROL Report] in de map [!UICONTROL Request Manager] . Zie [&#x200B; Naam een Verzoek &#x200B;](/help/analyze/legacy-report-builder/layout/name-a-request.md).

1. Klik op **[!UICONTROL OK]**.
