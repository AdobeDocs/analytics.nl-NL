---
description: Leer hoe u de offline modus kunt gebruiken om plaatsaanduidingsgegevens te retourneren.
title: Offlinemodus inschakelen
uuid: 4eb1f754-b6da-4896-a64f-b737563925b8
feature: Report Builder
role: User, Admin
exl-id: f18859e3-19e4-48af-963f-0bb4d1b46380
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# Offlinemodus voor het maken en bewerken van aanvragen

{{legacy-arb}}

In de offlinemodus worden plaatsaanduidingsgegevens geretourneerd om het maken en bewerken van aanvragen te versnellen.

Wanneer u een nieuwe aanvraag maakt of bewerkt, worden de API-aanroepen van het rapport gemaakt om de reactie op te halen. Soms vertragen deze vraag het proces van de verzoekverwezenlijking omdat u op de gegevens moet wachten om terug te keren alvorens naar de volgende stap te gaan. In de offlinemodus worden alleen plaatsaanduidingsgegevens geretourneerd en wordt geen API gemaakt.

Offlinemodus inschakelen

1. Klik op **[!UICONTROL Options]** in het menu Report Builder.

   ![&#x200B; Schermafbeelding van het scherm van Opties met offline geselecteerde code.](assets/offline_mode.png)

1. Schakel het selectievakje naast **[!UICONTROL Turn on offline mode for creating and editing requests]** in.
1. Voer in het veld **[!UICONTROL Display Metric Data as]** de plaatsaanduidingsgegevens in die u in uw aanvraag wilt retourneren. Voer bijvoorbeeld &quot;1&quot; in.
1. Klik op **[!UICONTROL OK]**.
1. Creeer en stel uw verzoek op off-line wijze in werking gebruikend de Tovenaar van het Verzoek. In de volgende schermafbeelding ziet u een voorbeeld van een aanvraag met &quot;1&quot; als plaatsaanduidingsgegevens.

   ![&#x200B; Schermafbeelding die het off-line wijzevoorbeeld toont gebruikend 1 als placeholder.](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >Zorg ervoor dat u de Offlinemodus uitschakelt voordat u uw aanvragen met echte gegevens uitvoert.
