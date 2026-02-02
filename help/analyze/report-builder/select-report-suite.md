---
title: Selecteer een rapportsuite in Report Builder
description: Leer hoe u een rapportsuite selecteert in Report Builder.
role: User
feature: Report Builder
type: Documentation
solution: Analytics
exl-id: 96e24d5d-78fb-4e5c-8513-c5fe221d0aeb
source-git-commit: 6f7de360ac24261eabb46c6cfce99449261706de
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 0%

---

# Selecteer een rapportsuite

U kunt een rapportsuite selecteren in het keuzemenu of een rapportsuite selecteren in een cel en uw gegevensblok automatisch bijwerken met een nieuwe rapportsuite.

## Rapportsuite selecteren vanuit een cel

Als u een rapportsuite in een cel selecteert, kunt u gegevensblokken eenvoudig vernieuwen met behulp van verschillende rapportsuites. In plaats van volledig nieuwe rapporten met afzonderlijke gegevensblokken te creëren, kunt u gegevensblokken met een rapportreeks verfrissen die van een cel wordt geselecteerd.

Het selecteren van een rapportsuite in een cel is handig als u:

* Meerdere rapportsuites die op elkaar lijken of identiek zijn in structuur.
* Gecompliceerde gegevensblokindelingen die aangepaste componenten en lay-outs bevatten.

Om een rapportreeks van een cel te selecteren, bouw eerst een gegevensblok en wijs veelvoudige rapportreeksen aan een cel buiten uw gegevensblok toe. Gebruik vervolgens het deelvenster **[!UICONTROL Report suite from cell]** om uw gegevensblokken te vernieuwen van verschillende rapportsuites.

1. Maak een gegevensblok. Voor informatie over het creëren van een gegevensblok, zie [&#x200B; een gegevensblok &#x200B;](/help/analyze/report-builder/create-a-data-block.md) creëren.

1. Selecteer ![&#x200B; DataViewSelector &#x200B;](/help/assets/icons/DataViewSelector.svg) in **[!UICONTROL Report suites]**.

1. Selecteer een cel gebruikend ![&#x200B; DataBlockSelector &#x200B;](/help/assets/icons/DataBlockSelector.svg) buiten het gegevensblok.

1. Voeg een of meer rapportsuites van **[!UICONTROL Select report suites to add to report suite from cell]** toe gebruikend belemmering en daling. U kunt ook een rapportsuite selecteren om de rapportsuite aan de lijst **[!UICONTROL Report suites included]** toe te voegen.

   * U kunt ![&#x200B; Onderzoek &#x200B;](/help/assets/icons/Search.svg) gebruiken **[!UICONTROL _Uitgezochte rapportsuites_]** om naar rapportsuites te zoeken.
   * Gebruik ![&#x200B; MoreSmall &#x200B;](/help/assets/icons/MoreSmall.svg) om een contextmenu te openen zodat kunt u rapportreeksen omhoog of omlaag in de **[!UICONTROL Report suites included]** lijst bewegen.
   * Gebruik ![&#x200B; CrossSize75 &#x200B;](/help/assets/icons/CrossSize75.svg) om een rapportreeks van de **[!UICONTROL Report suites included]** lijst te schrappen.

   ![&#x200B; Uitgezochte rapportreeks van een cel &#x200B;](assets/dataviews-from-a-cell.png){zoomable="yes"}

1. Selecteer **[!UICONTROL Apply]** om de geselecteerde rapportsuites op de geselecteerde cel toe te passen.


## De rapportsuite vanuit een cel wijzigen

1. Selecteer de locatie van de cel van de rapportsuite in uw werkblad.
1. Selecteer in de Report Builder-hub de koppeling **[!UICONTROL Report suites from cell]** in **[!UICONTROL Quick edit]** .
1. Selecteer een rapportsuite in het keuzemenu **[!UICONTROL Report suite]** .

   ![&#x200B; het rapportreeks van de Verandering van een cel &#x200B;](assets/change-data-view-from-cell.png){zoomable="yes"}
1. Selecteer **[!UICONTROL Refresh data block(s) upon change]** Optioneel.

1. Selecteer **[!UICONTROL Apply]** . Report Builder vernieuwt het gegevensblok op basis van de geselecteerde rapportsuite.
