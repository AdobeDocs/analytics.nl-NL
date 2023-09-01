---
description: Leer metriek toevoegen, verwijderen of vervangen in een reeds bestaand verzoek of over een groep verzoeken.
title: Hoe te om metriek over veelvoudige verzoeken uit te geven
feature: Report Builder
role: User, Admin
exl-id: e537b67a-aa07-4acd-a476-7497426e2f7d
source-git-commit: 66b7de0b008364e47253d319785c204ca479ab26
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Cijfers bewerken in meerdere aanvragen

Voeg, verwijder of vervang metriek in een reeds bestaand verzoek of over een groep verzoeken toe.

## Metrisch toevoegen {#section_3FBDA9668039404895059618D70FCBCD}

Houd rekening met de volgende richtlijnen wanneer u metriek toevoegt:

* Metrische gegevens kunnen alleen worden toegevoegd aan aanvragen voor draaitermindeling.
Als sommige van de geselecteerde aanvragen Aangepaste layouts zijn, kunnen geen metriek worden toegevoegd. Als de lay-out wordt aangepast, weet de Report Builder niet waar in spreadsheet om nieuwe metrisch te plaatsen.
* Als u alleen Aangepaste layout-aanvragen selecteert, worden de **[!UICONTROL Add Metrics]** is niet beschikbaar.
* Als u metriek toevoegt, wordt een aanvraag groter en kan dit ertoe leiden dat een andere aanvraag wordt overlapt. Zorg ervoor dat er voldoende ruimte is voor uw verzoek om metriek toe te voegen.
* Als toegevoegde metrisch reeds in één van de geselecteerde verzoeken aanwezig is, zal het niet aan dat verzoek worden toegevoegd.

Een of meer metriek toevoegen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om deze te selecteren **[!UICONTROL Edit Metrics]**. (Of klik op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > `<choose metric>` > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die moet worden gewijzigd.)
1. Selecteren **[!UICONTROL Add Metric(s)]**en selecteer de metriek om toe te voegen.

   ![Schermafbeelding met de optie Aanvraag bewerken, Metrisch(e) toevoegen geselecteerd.](assets/add_metric.png)

1. Vernieuw het verzoek om werkelijke gegevens te zien. Offlinegegevens worden weergegeven totdat u de gegevens vernieuwt.

## Metrische gegevens vervangen

Neem de volgende richtlijnen in acht wanneer u metriek vervangt:

* Alleen 1:1-substituties zijn toegestaan. 1:veel of veel:1 zijn niet toegestaan.
* Als de geselecteerde metrische waarde niet aanwezig is in een van de geselecteerde aanvragen, wordt het verzoek ongewijzigd gelaten.
* De nieuwe metrisch wordt geplaatst in de zelfde plaats zoals substituted metrisch.

   * **In een draaiende layout**, als een verzoek om een draaiende lay-out datum, bezoek, bezoekers, dagelijks uniek en *bezoekers* wordt vervangen door *inkomsten*, zal de bijgewerkte verzoeklay-out: datum, bezoek, opbrengst, en dagelijks uniek zijn.
   * **In een aangepaste layout**, als de *bezoekers* Metrisch werd output in cel F11, zal de bijgewerkte verzoeklay-out tonen *inkomsten* in dezelfde cel F11.

* Als op de vervangende metrische waarde een bewerking is toegepast (gemiddelde, vooraf toegevoegde tekst, tekst na opmaak, microcodering), worden deze bewerkingen ook op de nieuwe metrische waarde toegepast.

Een metrisch object vervangen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om deze te selecteren **[!UICONTROL Edit Metrics]**. U kunt ook op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > **`<choose metric>`** > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die moet worden gewijzigd.

1. Selecteren **[!UICONTROL Replace Metric]**.

   ![Screenshot van het scherm Groep bewerken met Metrisch vervangen geselecteerd.](assets/replace_metric.png)

1. Selecteer de metrische waarde die u wilt vervangen en de vervangende metrische waarde.
1. Vernieuw de aanvraag. Offlinegegevens worden weergegeven totdat u de gegevens vernieuwt.

## Metrische gegevens verwijderen {#section_D3CD5BAC7670416593B633B2B8423C60}

Houd rekening met de volgende richtlijnen wanneer u metriek verwijdert:

* Als een van de metriek die u voor verwijdering selecteert, niet aanwezig is in een van de geselecteerde aanvragen, blijft de aanvraag ongewijzigd.
* Als u in een draaiende layout een metrische waarde verwijdert, wordt de layout verschoven voor metrische gegevens die zich na de verwijderde metrische waarde bevinden. Bijvoorbeeld als een verzoek om de schermindeling Dravot datum, bezoeken, bezoekers, en dagelijks uniek uitbrengt, en u verwijdert *bezoeken* In de bijgewerkte lay-out voor de aanvraag worden vermeld: datum, bezoekers en dagelijkse unieke gegevens.

Metrische gegevens verwijderen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om deze te selecteren **[!UICONTROL Edit Metrics]**. U kunt ook op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > **`<choose metric>`** > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die moet worden gewijzigd.

1. Selecteren **[!UICONTROL Remove Metric(s)]**.

   ![Screenshot met de geselecteerde optie Groep bewerken en Metrisch(e) verwijderen.](assets/remove_metric.png)

1. Selecteer een of meer metriek die u uit de aanvraag wilt verwijderen.
1. Vernieuw de aanvraag. Tot u verfrist, zult u off-line gegevens zien.
