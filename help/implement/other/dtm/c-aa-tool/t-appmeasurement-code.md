---
description: Voeg toepassingsmetingscode in wanneer u handmatig Dynamic Tag Management in Adobe Analytics implementeert.
keywords: Dynamic Tag Management;linked accounts;linking accounts;edit code;appmeasurement;appmeasurement code
solution: Experience Cloud,Analytics,Target
title: Core AppMeasurement-code invoegen
uuid: 3f83fbb1-3ed5-4e45-888a-0a183aac1a90
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 5%

---


# Core AppMeasurement-code invoegen

Voeg toepassingsmetingscode in wanneer u handmatig Dynamic Tag Management in Adobe Analytics implementeert.

1. Vouw de [!DNL Adobe Analytics] sectie uit op de **[!UICONTROL General]** gereedschapspagina en klik op **[!UICONTROL Open Editor]**.
1. Pak het [!DNL AppMeasurement_JavaScript*.zip] bestand uit dat u hebt gedownload in [Adobe Analytics](/help/implement/other/dtm/t-analytics-deploy.md).

   Als u kiest voor een aangepaste bibliotheek, heeft deze bij het openen van het venster al de meest recente codeversie. Het is niet nodig om het ritje van de Admin Console te downloaden.
1. Openen [!DNL AppMeasurement.js] in een teksteditor.
1. Kopieer en plak de inhoud in het **[!UICONTROL Edit Code]** venster.

   ![](assets/edit-code.png)

1. Adobe raadt u aan de volgende code toe te voegen boven de *`Do Not Alter Anything Below This Line`*:

   ```
   var s_account="INSERT-RSID-HERE"
   var s=s_gi(s_account)
   ```

   >[!IMPORTANT]
   >
   >Als u deze code toevoegt, is het raadzaam ook het **[!UICONTROL Set report suites using custom code below]** selectievakje in de algemene bibliotheekinstellingen in te schakelen.

1. Klik op **[!UICONTROL Save and Close]**.

   Als u de Module van Media, de Module van de Integratie, of de implementatiestop-ins gebruikt, kunt u hen in de codesectie eveneens kopiëren. De beheerde code in Dynamisch Tagbeheer kan precies zoals het dossier JavaScript in een typische implementatie worden gevormd.

