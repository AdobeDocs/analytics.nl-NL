---
description: Afmetingen en dimensies in Analysis Workspace onderverdelen.
keywords: Analysis Workspace
title: Uitsplitsingsdimensies
feature: Dimensions
role: User, Admin
exl-id: 0d26c920-d0d9-4650-9cf0-b67dbc4629e1
source-git-commit: 10ae8213b8745439ab5968853f655a1176b8c38a
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 10%

---

# Uitsplitsingsdimensies

Afmetingen en dimensies in Analysis Workspace onderverdelen.

U kunt uw data onbeperkt voor al uw specifieke vereisten opsplitsen, query&#39;s bouwen met relevante metrics, dimensies, segmenten, tijdlijnen en andere uitsplitsingswaarden voor de analyse.

1. [Een project maken](/help/analyze/analysis-workspace/home.md) met een datatabel.
1. Klik in de gegevenstabel met de rechtermuisknop op een regelitem en selecteer **[!UICONTROL Breakdown]** > *`<item>`*.

   ![Stap Resultaat](assets/fa_data_table_actions.png)

   U kunt metriek onderverdelen door afmetingspunten of publiekssegmenten over geselecteerde tijdsperioden. U kunt ook verder naar beneden boren tot een meer korrelig niveau.

   >[!NOTE]
   >
   >Het aantal uitsplitsingen dat in de tabel moet worden weergegeven, is beperkt tot 200. Deze limiet neemt toe voor exportuitsplitsingen.

## Toewijzingsmodellen toepassen op uitsplitsingen

Voor elke uitsplitsing binnen een tabel kan ook een toewijzingsmodel worden toegepast. Dit attributiemodel kan hetzelfde zijn of verschillen van de bovenliggende kolom. Bijvoorbeeld, kunt u lineaire Orden op uw afmeting van de Kanalen van de Marketing analyseren maar U-Vormde Orden op de specifieke het volgen codes binnen een Kanaal toepassen. Als u het toewijzingsmodel wilt bewerken dat op een indeling is toegepast, plaatst u de muisaanwijzer boven het indelingsmodel en klikt u op **[!UICONTROL Edit]**:

![Onderbrekingsinstellingen](assets/breakdown_settings.png)

Dit is het verwachte gedrag wanneer het toepassen van attributiemodellen op onderverdelingen of het uitgeven van hen:

* Als u een attributie toepast terwijl er geen andere attributies bestaan, wordt de attributie toegepast op de gehele kolomstructuur.

* Als u een uitsplitsing toevoegt nadat een toewijzing is toegepast, wordt de standaardinstelling gebruikt voor de opgegeven uitsplitsing die is toegevoegd, als die dimensie een standaardinstelling heeft. Anders wordt de uitsplitsing van de bovenliggende kolom gebruikt. Sommige dimensies hebben een standaardtoewijzing.  Bijvoorbeeld: [!UICONTROL Time] afmetingen en [!UICONTROL Referrer] gebruiken [!UICONTROL Same Touch]. De [!UICONTROL Product] dimensies gebruiken [!UICONTROL Last Touch]. Andere afmetingen hebben geen gebrek, en zullen de toewijzing van de ouderkolom gebruiken.

* Als de kolomstructuur al kenmerken bevat, heeft het wijzigen van de toewijzing alleen invloed op de eigenschap die u bewerkt.

## Video&#39;s

Afmetingen en metriek toevoegen aan uw project in Analysis Workspace:

>[!VIDEO](https://video.tv.adobe.com/v/30606/?quality=12)

Werken met afmetingen in een tabel voor vrije vorm:

>[!VIDEO](https://video.tv.adobe.com/v/40179/?quality=12)

Hier volgt een video over afmetingsonderverdelingen op positie:

>[!VIDEO](https://video.tv.adobe.com/v/24033/?quality=12)
