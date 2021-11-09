---
title: Meerdere rapportsuites
description: Leer hoe en waarom u projecten maakt in Workspace met meerdere rapportsuite
feature: Workspace Basics
role: User, Admin
exl-id: 0429ddd9-935f-44ef-ae1e-97bb02e6e2df
source-git-commit: 76af5908fd65cae26106ca9c1a71978624a77320
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# Meerdere rapportsuites

U kunt nu projecten in Analysis Workspace maken met gegevens uit meerdere rapportenpakketten. De reeksen van het rapport worden nu gekozen op het paneelniveau, zodat kunt u een verschillende rapportreeks voor elk paneel binnen het zelfde project van de Werkruimte kiezen.

Deze mogelijkheid is handig als u bijvoorbeeld

* Vergelijk gegevens uit twee verschillende gebieden en de gegevens bevinden zich in twee verschillende rapportsuites. U kunt tabellen en visualisaties maken om de gegevens naast elkaar te vergelijken.

* Bouw een dashboard van metriek en visualisaties om uit te melden aan andere organisaties. U kunt nu gegevens van diverse rapportsuites in het zelfde project trekken.

Hier is een video over het onderwerp:

>[!VIDEO](https://video.tv.adobe.com/v/32843/?quality=12)

## Rapportsuite toepassen op alle deelvensters

U kunt een rapportsuite op alle deelvensters tegelijk toepassen door met de rechtermuisknop op de koptekst van een deelvenster te klikken en **[!UICONTROL Apply Report Suite to All Panels]**.

![](assets/apply-rs-all-panels.png)

## Actief deelvenster

Met deze functie introduceren we het concept &quot;actief panel&quot; in plaats van &quot;inactief panel&quot;. U kunt het actieve deelvenster herkennen aan de lichtblauwe rand eromheen. Als u gewoon in een deelvenster klikt, wordt dat deelvenster omgezet in het actieve deelvenster.

>[!IMPORTANT]
>U kunt slepen en neerzetten in elk deelvenster dat zich in dezelfde rapportsuite bevindt als het actieve deelvenster. Door naar een inactief deelvenster van dezelfde rapportsuite te slepen, wordt het deelvenster actief.

| Taak | Actief deelvenster | Inactief deelvenster |
| --- | --- | --- |
| Rapportsuite wijzigen | Ja | Nee |
| Componenten slepen en neerzetten | Ja | Ja, voor elk deelvenster dat zich in dezelfde rapportsuite bevindt als uw actieve deelvenster. |
| Visualisaties slepen en neerzetten | Ja | Ja, voor elk deelvenster dat zich in dezelfde rapportsuite bevindt als uw actieve deelvenster. |

## Werken met meerdere rapportsuites

![](assets/mrs-ui.png)

1. Maak een nieuw project met twee of meer deelvensters in Workspace.

1. Sleep componenten (maateenheden, afmetingen, segmenten, datumbereiken) naar het deelvenster. Zorg ervoor dat deelvensters gegevens en visualisaties hebben die specifiek zijn voor hun rapportsuite.


   >[!NOTE]
   >Soms wordt een banner weergegeven tijdens het laden van een project (of het overschakelen naar een rapportsuite), waarbij niet alle componenten die in het project zijn opgenomen, in de rapportsuite zijn opgenomen. De ontbrekende componenten worden weergegeven. Volg [deze instructies](/help/admin/admin-console/permissions/product-profile.md) om machtigingen in te stellen voor de vereiste maateenheden/afmetingen.

   ![](assets/incompat-rs.png)

   U hebt drie opties om deze incompatibiliteit te verhelpen:
   * De vereiste afmetingen/metriek inschakelen
   * Wijzig de rapportsuite.
   * Doorgaan met enkele ontbrekende componenten. Dit resulteert in geen gegevens voor die componenten, en/of lege visualisaties.

1. Wijzig het deelvenster in een andere rapportsuite. U ziet hoe het componentlabel (momenteel actieve rapportsuite) en de weergegeven componenten worden bijgewerkt op basis van de nieuwe rapportsuite.

1. Een sneltoets gebruiken (`shift` tijdens het slepen) om een inactief deelvenster om te zetten in een actief deelvenster.

1. (Optioneel) U kunt ook naar andere componentbuilders van Analytics gaan en ervoor zorgen dat deze nu een label van een rapportsuite tonen die

   * Waar wordt een segment gemaakt: [Segment Builder](https://experienceleague.adobe.com/docs/analytics/components/segmentation/segmentation-workflow/seg-build.html).
   * Wanneer een berekende metrische waarde wordt gecreëerd: [Berekende metrische bouwer](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html).
   * Wanneer een waarschuwing wordt opgesteld: [Alert Builder](https://experienceleague.adobe.com/docs/analytics/components/alerts/alert-builder.html).
