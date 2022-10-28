---
description: In de offlinemodus worden plaatsaanduidingsgegevens geretourneerd om het maken en bewerken van aanvragen te versnellen.
title: Offline modus voor het maken en bewerken van aanvragen
uuid: 4eb1f754-b6da-4896-a64f-b737563925b8
feature: Report Builder
role: User, Admin
exl-id: f18859e3-19e4-48af-963f-0bb4d1b46380
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 8%

---

# Offline modus voor het maken en bewerken van aanvragen

In de offlinemodus worden plaatsaanduidingsgegevens geretourneerd om het maken en bewerken van aanvragen te versnellen.

Wanneer u nieuw verzoek creeert of uitgeeft, worden de vraag van rapport API gemaakt om de reactie terug te winnen. Hierdoor wordt het maken van aanvragen vertraagd, omdat u moet wachten tot de gegevens zijn geretourneerd voordat u naar de volgende stap gaat. In de offlinemodus worden alleen plaatsaanduidingsgegevens geretourneerd, zodat er geen API-aanroepen hoeven te worden uitgevoerd.

Offlinemodus inschakelen:

1. Klikken **[!UICONTROL Options]** in het menu Report Builder.

   ![Offlinemodus](assets/offline_mode.png)

1. Schakel het selectievakje naast **[!UICONTROL Turn on offline mode for creating and editing requests]**.
1. In de **[!UICONTROL Display Metric Data as]** voert u in uw verzoek de gegevens in voor de tijdelijke aanduiding die u wilt retourneren. Voer bijvoorbeeld &quot;1&quot; in.
1. Klik op **[!UICONTROL OK]**.
1. Creëer nu en stel uw verzoek (op off-line wijze) in werking gebruikend de Tovenaar van het Verzoek.
1. Uw verzoek met &#39;1&#39; als plaatsaanduidingsgegevens ziet er ongeveer als volgt uit:

   ![Voorbeeld van offlinemodus](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >Zorg ervoor dat u de Offlinemodus uitschakelt voordat u uw aanvragen met echte gegevens uitvoert. Ga hiervoor gewoon terug naar **[!UICONTROL Options]** en verwijder het vinkje.
