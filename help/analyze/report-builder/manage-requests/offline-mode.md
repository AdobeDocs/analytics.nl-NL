---
description: In de offlinemodus worden plaatsaanduidingsgegevens geretourneerd om het maken en bewerken van aanvragen te versnellen.
title: Offline modus voor het maken en bewerken van aanvragen
uuid: 4eb1f754-b6da-4896-a64f-b737563925b8
feature: Report Builder
role: User, Admin
exl-id: f18859e3-19e4-48af-963f-0bb4d1b46380
source-git-commit: 7226b4c77371b486006671d72efa9e0f0d9eb1ea
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 9%

---

# Offline modus voor het maken en bewerken van aanvragen

In de offlinemodus worden plaatsaanduidingsgegevens geretourneerd om het maken en bewerken van aanvragen te versnellen.

Wanneer u nieuw verzoek creeert of uitgeeft, worden de vraag van rapport API gemaakt om de reactie terug te winnen. Hierdoor wordt het maken van aanvragen vertraagd, omdat u moet wachten tot de gegevens zijn geretourneerd voordat u naar de volgende stap gaat. In de offlinemodus worden alleen plaatsaanduidingsgegevens geretourneerd, zodat er geen API-aanroepen hoeven te worden uitgevoerd.

Offlinemodus inschakelen:

1. Klik **[!UICONTROL Options]** in het menu van de Report Builder.

   ![](assets/offline_mode.png)

1. Schakel het selectievakje naast **[!UICONTROL Turn on offline mode for creating and editing requests]** in.
1. Voer in het veld **[!UICONTROL Display Metric Data as]** de plaatsaanduidingsgegevens in die u in uw verzoek wilt retourneren. Voer bijvoorbeeld &quot;1&quot; in.
1. Klik op **[!UICONTROL OK]**.
1. Creëer nu en stel uw verzoek (op off-line wijze) in werking gebruikend de Tovenaar van het Verzoek.
1. Uw verzoek met &#39;1&#39; als plaatsaanduidingsgegevens ziet er ongeveer als volgt uit:

   ![](assets/offline_mode_example.png)

   >[!IMPORTANT]
   >
   >Zorg ervoor u Off-line Wijze onbruikbaar maakt alvorens uw verzoeken met echte gegevens in werking te stellen. Ga hiertoe gewoon terug naar **[!UICONTROL Options]** en verwijder het vinkje.
