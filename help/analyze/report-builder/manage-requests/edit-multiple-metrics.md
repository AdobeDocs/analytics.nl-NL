---
description: Met de functie Metrische gegevens bewerken in meerdere verzoeken kunt u eenvoudig metrische gegevens toevoegen, verwijderen of vervangen in een bestaande aanvraag of in een groep verzoeken.
title: Metriek bewerken in meerdere verzoeken
uuid: 50fba4e7-ca7d-4a5c-98a9-c9725b436e4a
translation-type: tm+mt
source-git-commit: 52cc111c0f28b099f038e4b6c69a9431fe506111

---


# Metriek bewerken in meerdere verzoeken

Met de functie Metrische gegevens bewerken in meerdere verzoeken kunt u eenvoudig metrische gegevens toevoegen, verwijderen of vervangen in een bestaande aanvraag of in een groep verzoeken.

## Metrisch toevoegen {#section_3FBDA9668039404895059618D70FCBCD}

Houd er rekening mee dat

* Metrische gegevens kunnen alleen worden toegevoegd aan aanvragen voor draaitermindeling. Als sommige van de geselecteerde aanvragen Aangepaste layouts zijn, kunnen geen metriek worden toegevoegd. De reden is dat de Bouwer van het Rapport niet weet waar in spreadsheet om nieuwe metrisch te plaatsen, aangezien de lay-out wordt aangepast.
* Als u dus alleen Aangepaste layout-aanvragen hebt geselecteerd, is de **[!UICONTROL Add Metric/s]** optie niet beschikbaar.
* Door het toevoegen van metrisch/s wordt een aanvraag groter en kan dit overlappen met een ander verzoek. Zorg ervoor dat er voldoende ruimte is voor uw verzoek om metriek toe te voegen.
* Als de toegevoegde metrische waarde al aanwezig is in een van de geselecteerde aanvragen, wordt deze niet toegevoegd aan dat verzoek.

Een of meer metriek toevoegen:

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om deze te selecteren **[!UICONTROL Edit Metrics]**. (Of klik op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > `<choose metric>` > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die u wilt wijzigen.)
1. Selecteer **[!UICONTROL Add Metric(s)]**en selecteer de metriek om toe te voegen.

   ![](assets/add_metric.png)

1. Vernieuw het verzoek om werkelijke gegevens te zien. Tot u verfrist, zult u off-line gegevens zien.

## Metrisch vervangen {#section_D773AAC7B30C4FBEBDB66B203C217818}

Houd er rekening mee dat

* Slechts 1:1 substituties zijn toegestaan, niet 1:veel of vele:1.
* Als de gekozen metrische waarde niet in een van de geselecteerde aanvragen voorkomt, blijft deze aanvraag ongewijzigd.
* De nieuwe metrische waarde wordt op dezelfde locatie geplaatst als de vervangen metrische waarde. Dit betekent:

   * **In een draaiende layout**: als een pivot layout aanvragen voor uitvoer datum , bezoek , bezoekers , dagelijks unieke en &quot; bezoekers &quot; wordt vervangen door &quot; inkomsten &quot; , wordt de bijgewerkte aanvraagindeling als volgt gewijzigd : datum, bezoek, inkomsten, dagelijks uniek.
   * **In een aangepaste layout**: als de metrische waarde &quot;bezoekers&quot; wordt weergegeven in cel F11, wordt in de bijgewerkte aanvraagindeling &quot;inkomsten&quot; weergegeven in dezelfde cel F11.

* Als op de vervangende metrische waarde een bewerking is toegepast (gemiddelde, vooraf toegevoegde tekst, tekst na opmaak, microcodering), worden deze bewerkingen ook op de nieuwe metrische waarde toegepast.

Een metrisch object vervangen

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om deze te selecteren **[!UICONTROL Edit Metrics]**. (Of klik op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > **`<choose metric>`** > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die u wilt wijzigen.)

1. Selecteer **[!UICONTROL Replace Metric]**.

   ![](assets/replace_metric.png)

1. Selecteer welke metrische waarde moet worden vervangen en welke metrische waarde deze vervangt.
1. Vernieuw de aanvraag. Tot u verfrist, zult u off-line gegevens zien.

## Metrische gegevens verwijderen {#section_D3CD5BAC7670416593B633B2B8423C60}

Houd er rekening mee dat

* Als een van de geselecteerde meetgegevens niet aanwezig is in een van de geselecteerde aanvragen, blijft deze aanvraag ongewijzigd.
* Als u een metrische waarde verwijdert in een draaitout, wordt de layout verschoven voor metrische gegevens die zich na de verwijderde metrische waarde bevinden.

   **Voorbeeld**: als een de outputdatum, bezoeken, bezoekers, dagelijks uniek en u &quot;bezoeken&quot;verwijdert van een draaiende lay-out, zal de bijgewerkte lay-out voor het verzoek tonen: datum, bezoekers, dagelijks uniek.

Metrische gegevens verwijderen:

1. Selecteer een of meer aanvragen in Excel en klik met de rechtermuisknop om deze te selecteren **[!UICONTROL Edit Metrics]**. (Of klik op **[!UICONTROL Manage]** > **[!UICONTROL Edit Multiple]** > **`<choose metric>`** > **[!UICONTROL Edit Group]** om de groep verzoeken te selecteren die u wilt wijzigen.)

1. Selecteer **[!UICONTROL Remove Metric(s)]**.

   ![](assets/remove_metric.png)

1. Selecteer een of meer metriek die u uit de aanvraag wilt verwijderen.
1. Vernieuw de aanvraag. Tot u verfrist, zult u off-line gegevens zien.

