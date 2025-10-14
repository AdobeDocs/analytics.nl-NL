---
description: Leer metriek toevoegen, verwijderen of vervangen in een reeds bestaand verzoek of over een groep verzoeken.
title: Hoe te om metriek over veelvoudige verzoeken uit te geven
feature: Report Builder
role: User, Admin
exl-id: e537b67a-aa07-4acd-a476-7497426e2f7d
source-git-commit: fcecc8a493852f5682fd7fbd5b9bb484a850922c
workflow-type: tm+mt
source-wordcount: '563'
ht-degree: 0%

---

# Metriek bewerken in meerdere verzoeken

{{legacy-arb}}

Voeg, verwijder of vervang metriek in een reeds bestaand verzoek of over een groep verzoeken toe.

## Metrisch toevoegen {#section_3FBDA9668039404895059618D70FCBCD}

Houd rekening met de volgende richtlijnen wanneer u metriek toevoegt:

* Metrische gegevens kunnen alleen worden toegevoegd aan aanvragen voor draaitermindeling.
Als sommige van de geselecteerde aanvragen Aangepaste layouts zijn, kunnen geen metriek worden toegevoegd. Als de lay-out wordt aangepast, weet de Report Builder niet waar in spreadsheet om nieuwe metrisch te plaatsen.
* Als u alleen Aangepaste layout-aanvragen selecteert, is de optie **[!UICONTROL Add Metrics]** niet beschikbaar.
* Als u metriek toevoegt, wordt een aanvraag groter en kan dit ertoe leiden dat een andere aanvraag wordt overlapt. Zorg ervoor dat er voldoende ruimte is voor uw verzoek om metriek toe te voegen.
* Als toegevoegde metrisch reeds in één van de geselecteerde verzoeken aanwezig is, zal het niet aan dat verzoek worden toegevoegd.

Een of meer metriek toevoegen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om **[!UICONTROL Edit Metrics]** te selecteren. (Of klik op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > `<choose metric>` > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die u wilt wijzigen.)
1. Selecteer **[!UICONTROL Add Metric(s)]**&#x200B;en selecteer de metriek om toe te voegen.

   ![&#x200B; Schermafbeelding die het Edit Verzoek toont, voegt Geselecteerde optie Metriek(en) toe.](assets/add_metric.png)

1. Vernieuw het verzoek om werkelijke gegevens te zien. Offlinegegevens worden weergegeven totdat u de gegevens vernieuwt.

## Metrische gegevens vervangen

Neem de volgende richtlijnen in acht wanneer u metriek vervangt:

* Alleen 1:1-substituties zijn toegestaan. 1:veel of veel:1 zijn niet toegestaan.
* Als de geselecteerde metrische waarde niet aanwezig is in een van de geselecteerde aanvragen, wordt het verzoek ongewijzigd gelaten.
* De nieuwe metrisch wordt geplaatst in de zelfde plaats zoals substituted metrisch.

   * **in een Lay-out van de Draaiende**, als een datum van het de outputs van de pivotlay-out verzoek, bezoekers, dagelijkse unieke en *bezoekers* door *opbrengst* wordt vervangen, zal de bijgewerkte verzoeklay-out: datum, bezoek, opbrengst, en dagelijks uniek zijn.
   * **in een Lay-out van de Douane**, als *bezoekers* metrisch in cel F11 werd uitgevoerd, zal de bijgewerkte verzoeklay-out *opbrengst* in zelfde cel F11 tonen.

* Als op de vervangende metrische waarde een bewerking is toegepast (gemiddelde, vooraf toegevoegde tekst, tekst na opmaak, microcodering), worden deze bewerkingen ook op de nieuwe metrische waarde toegepast.

Een metrisch object vervangen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om **[!UICONTROL Edit Metrics]** te selecteren. U kunt ook op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > **`<choose metric>`** > **[!UICONTROL Edit Group]** klikken om de groep verzoeken te selecteren die u wilt wijzigen.

1. Selecteer **[!UICONTROL Replace Metric]** .

   ![&#x200B; Schermafbeelding van het Edit scherm van de Groep met Replace Metric geselecteerd.](assets/replace_metric.png)

1. Selecteer de metrische waarde die u wilt vervangen en de vervangende metrische waarde.
1. Vernieuw de aanvraag. Offlinegegevens worden weergegeven totdat u de gegevens vernieuwt.

## Metrische gegevens verwijderen {#section_D3CD5BAC7670416593B633B2B8423C60}

Houd rekening met de volgende richtlijnen wanneer u metriek verwijdert:

* Als een van de metriek die u voor verwijdering selecteert, niet aanwezig is in een van de geselecteerde aanvragen, blijft de aanvraag ongewijzigd.
* Als u in een draaiende layout een metrische waarde verwijdert, wordt de layout verschoven voor metrische gegevens die zich na de verwijderde metrische waarde bevinden. Bijvoorbeeld, als een de outputdatum van het de lay-outverzoek van de pivot, bezoeken, bezoekers, en dagelijks uniek, en u *bezoeken* verwijdert, zal de bijgewerkte lay-out voor het verzoek tonen: datum, bezoekers, en dagelijks uniek.

Metrische gegevens verwijderen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om **[!UICONTROL Edit Metrics]** te selecteren. U kunt ook op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > **`<choose metric>`** > **[!UICONTROL Edit Group]** klikken om de groep verzoeken te selecteren die u wilt wijzigen.

1. Selecteer **[!UICONTROL Remove Metric(s)]** .

   ![&#x200B; Schermafbeelding die de Edit Groep tonen en geselecteerde optie Metrisch(e) verwijderen.](assets/remove_metric.png)

1. Selecteer een of meer metriek die u uit de aanvraag wilt verwijderen.
1. Vernieuw de aanvraag. Tot u verfrist, zult u off-line gegevens zien.
