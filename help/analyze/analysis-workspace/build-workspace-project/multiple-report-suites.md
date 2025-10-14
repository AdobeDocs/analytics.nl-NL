---
title: Meerdere rapportsets
description: Leer hoe u met meerdere rapportensuites werkt in één Analysis Workspace-project.
feature: Workspace Basics
role: User, Admin
exl-id: 0429ddd9-935f-44ef-ae1e-97bb02e6e2df
source-git-commit: 665319bdfc4c1599292c2e7aea45622d77a291a7
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 0%

---

# Meerdere rapportsuites

U kunt projecten in Analysis Workspace maken met gegevens uit meerdere rapportsuite. De reeksen van het rapport worden gekozen op paneelniveau, zodat kunt u een verschillende rapportreeks voor elk paneel binnen het zelfde project van Workspace kiezen.

Deze mogelijkheid is handig als u wilt:

* Vergelijk gegevens uit twee verschillende gebieden en de gegevens bevinden zich in twee verschillende rapportsuites. U kunt tabellen en visualisaties maken om de gegevens naast elkaar te vergelijken.

* Bouw een dashboard van metriek en visualisaties om uit te melden aan andere organisaties. U kunt gegevens van diverse rapportreeksen in het zelfde project trekken.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; Veelvoudige rapportsuites &#x200B;](https://video.tv.adobe.com/v/32843?quality=12&learn=on){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Rapportsuite toepassen op alle deelvensters

U kunt een rapportsuite op alle deelvensters tegelijk toepassen door met de rechtermuisknop op de koptekst van een deelvenster te klikken en **[!UICONTROL Apply Report Suite to All Panels]** te selecteren.

![](assets/apply-rs-all-panels.png)

## Actief deelvenster

U kunt het actieve deelvenster herkennen aan de lichtblauwe rand eromheen. Selecteer in een deelvenster om dat deelvenster om te zetten in het actieve deelvenster.

>[!TIP]
>
>U kunt slepen en neerzetten in elk deelvenster dat zich in dezelfde rapportsuite bevindt als het actieve deelvenster. Door naar een inactief deelvenster van dezelfde rapportsuite te slepen, wordt het deelvenster actief.
>

## Werken met meerdere rapportsuites

![](assets/mrs-ui.png)

1. Maak een nieuw project met twee of meer deelvensters in Workspace.

1. Sleep componenten (maateenheden, afmetingen, segmenten, datumbereiken) naar het deelvenster. Zorg ervoor dat deelvensters gegevens en visualisaties hebben die specifiek zijn voor hun rapportsuite.


   >[!NOTE]
   >
   >Soms wordt een banner weergegeven tijdens het laden van een project (of het overschakelen naar een rapportsuite), waarbij niet alle componenten die in het project zijn opgenomen, in de rapportsuite zijn opgenomen. De ontbrekende componenten worden weergegeven. Volg [&#x200B; deze instructies &#x200B;](/help/admin/admin-console/permissions/product-profile.md) om toestemmingen aan de vereiste metriek/afmetingen te plaatsen.
   >

   ![](assets/incompat-rs.png)

   U hebt drie opties om deze incompatibiliteit te verhelpen:
   * De vereiste afmetingen/metriek inschakelen
   * Wijzig de rapportsuite.
   * Doorgaan met enkele ontbrekende componenten. Dit resulteert in geen gegevens voor die componenten, en/of lege visualisaties.

1. Wijzig het deelvenster in een andere rapportsuite. U ziet hoe het componentlabel (momenteel actieve rapportsuite) en de weergegeven componenten worden bijgewerkt op basis van de nieuwe rapportsuite.

1. Gebruik een sneltoets (`shift` tijdens het slepen) om een inactief deelvenster om te zetten in een actief deelvenster.

1. (Optioneel) U kunt ook naar andere componentbuilders van Analytics gaan en ervoor zorgen dat deze nu een label van een rapportsuite tonen die

   * Waar een segment zal worden gecreeerd: [&#x200B; de bouwer van het Segment &#x200B;](/help/components/segmentation/segmentation-workflow/seg-build.md).
   * Waar berekende metrisch zal worden gecreeerd: [&#x200B; Berekende metrische bouwer &#x200B;](/help/components/calculated-metrics/workflow/c-build-metrics/cm-build-metrics.md).
   * Waar een alarm zal worden gebouwd: [&#x200B; Alert bouwer &#x200B;](/help/components/alerts/alert-builder.md).
