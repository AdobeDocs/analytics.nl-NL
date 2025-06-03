---
title: Betaalde zoekgegevens importeren
description: Stappen om Adobe Analytics te configureren voor het bijhouden van uw betaalde zoekgegevens (bijvoorbeeld Google Ads, Microsoft Advertising, enz.) met behulp van gegevensbronnen.
exl-id: b25a2a26-d277-4a51-9194-973acb425095
feature: Data Sources
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '1099'
ht-degree: 0%

---

# [!UICONTROL Paid Search] metriek importeren met [!UICONTROL Data Sources]

Voor veel marketingorganisaties is betaalde zoekopdrachten een van de meest waardevolle en betrouwbare manieren &#x200B; nieuwe klanten te bereiken en bestaande klanten te behouden. Met de [!UICONTROL Data Sources] -functie in Adobe Analytics kunt u eenvoudig geavanceerde, betaalde zoekgegevens importeren van digitale advertentieplatforms zoals Google Ads. U kunt het met de rest van uw marketing gegevens, naast het gedrag en de gegevens van de klantenattributen ter plaatse integreren, om u betere inzichten in de betaalde onderzoeksinspanningen van uw organisatie toe te staan.

Deze stappen tonen u hoe te om een integratie met Ads te vormen om sleutelwoordgegevens evenals metriek zoals indrukken, kliks, kosten per klik, en meer in te voeren.

In de stappen wordt uitgelegd hoe u een eenmalige import van gegevens met een pay-per-click instelt. In [!UICONTROL Data Sources] kunt u echter gegevens blijven importeren in de bestandsindeling die hier wordt beschreven. Afhankelijk van uw betaalde zoekplatform kunt u mogelijk periodieke exportbewerkingen (dagelijks, maandelijks, enz.) plannen, geautomatiseerde processen instellen om deze exportbewerkingen om te zetten in de bestandsindeling die Adobe Analytics nodig heeft, en deze bestanden uploaden naar Adobe Analytics voor de rapportage van betaalde zoekintegratie.

## Vereisten

* U hebt betaalde zoekdetectie geïmplementeerd.
* U vangt het volgen codegegevens.
* U hebt unieke volgcodes voor elke advertentiegroep.

## Configureren [!UICONTROL Success Events]

Onze eerste stap is om Adobe Analytics voor te bereiden op het ontvangen van de cijfers. Hiervoor moet u een aantal succesgebeurtenissen instellen.

[!UICONTROL Success events] zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een [!UICONTROL success event] is. Voor het bijhouden van [!UICONTROL paid search] -metriek willen we [!UICONTROL success events] rondom [!UICONTROL clicks] , [!UICONTROL impressions] [!UICONTROL total cost] instellen en [!UICONTROL tracking codes] inschakelen.

1. Ga naar **[!UICONTROL Adobe Analytics > Admin > Report Suites]** .
1. Selecteer een rapportsuite.
1. Klik op **[!UICONTROL Edit Settings > Conversion > Success Events]**.

   ![ Gebeurtenissen van het Succes ](assets/success-events.png)

1. Gebruik **[!UICONTROL Add New]** onder Aangepaste succesgebeurtenissen om 3 aangepaste succesgebeurtenissen te maken: [!UICONTROL Clicks] (Teller), [!UICONTROL Impressions] (Teller) en [!UICONTROL Total Cost] (Valuta).

   ![ Nieuwe succesgebeurtenis ](assets/new-success-events.png)

1. Klik op Opslaan.
Je ontvangt een bericht dat je bespaart is goedgekeurd.
1. Navigeer naar **[!UICONTROL Admin > Report Suites > Edit Settings > Conversion > Conversion Variables]** .
1. Schakel volgcodes in door het selectievakje naast **[!UICONTROL Tracking Code]** onder **[!UICONTROL Campaign > Campaign Variable]** in te schakelen.

   ![ variabele van de Campagne ](assets/campaign-variable.png)

## Gegevensbronnen instellen

Met [!UICONTROL Data Sources] kunt u niet-klikstreamgegevens delen met Adobe Analytics. In dit geval gebruiken we Adobe Analytics om betaalde zoekgegevens bij te houden. We gebruiken de trackingcode als onze sleutel om de twee stukken gegevens - betaalde zoekgegevens en Adobe Analytics-meetgegevens - samen te voegen.

1. Navigeer naar **[!UICONTROL Adobe Analytics > Admin > All admin > Data sources]** .
1. Selecteer het tabblad **[!UICONTROL Create]** om nieuwe gegevensbronnen te activeren.
1. Selecteer onder **[!UICONTROL Select Category]** de optie **[!UICONTROL Ad Campaign]** .

   ![Databronnen](assets/data-sources.png)

1. Selecteer onder **[!UICONTROL Select Type]** de optie **[!UICONTROL Generic Pay-Per-Click Service]** .
1. Klik op **[!UICONTROL Activate]** .
In [!UICONTROL Data Source Activation Wizard] wordt het volgende weergegeven:

   ![ Tovenaar van de Activering ](assets/ds-activation-wizard.png)

1. Klik op **[!UICONTROL Next]** en geef de gegevensbron een naam. Deze naam wordt weergegeven in Data Source Manager.
1. Accepteer de serviceovereenkomst en klik op **[!UICONTROL Next]** .
1. Selecteer de drie standaardmetriek: [!UICONTROL Impressions] , [!UICONTROL Clicks] en [!UICONTROL Total Cost] en klik op **[!UICONTROL Next]** .
1. Nu &quot;kaart&quot;deze nieuwe gegevensbron aan de douanegebeurtenissen die wij in [ gebeurtenissen van het Succes ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/success-event.md) creeerden.

   ![ Toewijzing ](assets/data-source-mapping.png)

1. Gegevensafmetingen kiezen
Schakel het vakje naast Bijkomende codes in en klik op **[!UICONTROL Next]** .
1. Afmetingen van kaartgegevens.
Wijs de geïmporteerde gegevensdimensie (kenmerk) toe aan het Adobe Analytics-kenmerk waarin u het wilt opslaan. Dit kan een standaardafmeting of een eVar zijn. Nadat u op **[!UICONTROL Next]** hebt geklikt, worden de resulterende toewijzingen weergegeven in het overzicht:

   ![ Samenvatting ](assets/data-source-summary.png)

1. Klik op **[!UICONTROL Save]**.
1. Klik op **[!UICONTROL Download]** om het sjabloonbestand voor deze gegevensbron te downloaden.
De bestandsnaam komt overeen met het type gegevensbron dat u oorspronkelijk hebt opgegeven, in dit geval &quot;Algemene Pay-per-Click service template.txt&quot;.
1. Open de sjabloon in uw favoriete teksteditor.
Het bestand is al gevuld met de meetwaarden en afmetingen en de bijbehorende toewijzingen.

## PPC-gegevens exporteren en uploaden naar Analytics

Stappen die vergelijkbaar zijn met deze bewerkingen voor Google Ads, Microsoft Advertising en andere PPC-accounts.

### Gegevens exporteren

1. Meld u aan bij uw PPC-account en maak een nieuw rapport of exporteer het bestand.
Zorg ervoor dat het exporteren de volgende velden bevat: datum, doel-URL (bestemmingspagina), afbeeldingen, klikken en kosten. Het exporteren kan andere velden bevatten, maar u verwijdert deze door de onderstaande stappen te volgen.
1. Sla indien mogelijk het rapport op als een `.csv` - of tabgescheiden bestand. Hierdoor wordt het gemakkelijker om met de volgende stappen te werken.
1. Open het bestand in Microsoft Excel.

### Het bestand bewerken in Microsoft Excel

1. Verwijder in Microsoft Excel alle andere kolommen dan de hierboven vermelde.
1. Verwijder eventuele extra rijen bovenaan.
1. De volgende codes isoleren van de doel-URL&#39;s:
a. Kopieer en plak gegevens uit alle kolommen.
b. Klik op **[!UICONTROL Data > Text to Columns]** .
c. Controleer of in Stap 1 van de wizard **[!UICONTROL Delimited]** is geselecteerd en klik op **[!UICONTROL Next]** .
d. Geef in Stap 2 van de wizard het scheidingsteken op, afhankelijk van de manier waarop u de URL&#39;s hebt gemaakt (of ? of &amp;) en klik op **[!UICONTROL Next]** .
e. In Stap 3 van de tovenaar, voorproef uw gegevens en zorg ervoor dat één van de kolommen &quot;trackingcodename=trackingcode&quot;is. Herhaal deze stappen (met &amp; als scheidingsteken) als u aanvullende variabelen hebt.
f. Verwijder alle kolommen, behalve voor trackingcodes, afbeeldingen, klikken en kosten. Voeg een nieuwe kolom toe genoemd Datum en organiseer uw kolommen in de volgende orde: Datum:: het Volgen code::: Impressies:: Klik: Kosten.
1. Voeg deze gegevens aan het malplaatje toe u in de &quot;van de Instelling Gegevensbronnen&quot;sectie hierboven downloadde.
U kunt het bestand nu uploaden.

### Bestand uploaden naar Adobe Analytics via FTP

Ga terug naar de wizard Data Source voor instructies en upload het bestand via FTP:

![ uploadt FTP ](assets/upload-ftp.png)

## Berekende waarden maken

Het toevoegen van berekende metriek zal nuttig zijn wanneer het maken van loon-per-klikbesluiten.

Bijvoorbeeld, kon u deze [ berekende metriek ](https://experienceleague.adobe.com/docs/analytics/components/calculated-metrics/calcmetric-workflow/cm-build-metrics.html#calculated-metrics) toevoegen:

| Naam | Formule | Metrisch type | Beschrijving |
| --- | --- | --- | --- |
| Paginaweergaven per bezoek | Paginaweergaven/bezoeken | Numeriek | Bij toepassing op siteniveau: het gemiddelde aantal pagina&#39;s per bezoek. Wanneer toegepast in het rapport Populaire pagina&#39;s: geeft het gemiddelde aantal keer weer dat een specifieke pagina per bezoek is bekeken. |
| Gemiddelde bestelwaarde | Ontvangsten/bestellingen | Valuta | Toont gemiddelde opbrengst per orde. |
| Ontvangsten per bezoek | Ontvangsten/bezoeken | Valuta | Toont gemiddelde opbrengst per bezoek. |
| Doorkliksnelheid (CTR) | Klikken/impressies | Numeriek | Meet de verhouding van kliks tot beelden van een online advertentie of e-mailmarketing campagne. |
| Winst | Ontvangsten - kosten | Valuta | Toont de opbrengst van een campagne minus de kosten. |
| Winst per impressie (PPI) | (Ontvangsten - kosten)/druk | Valuta | Toont hoeveel opbrengst elke keer werd geproduceerd een advertentie, evenwichtig met kosten. |
| Retourneren op advertentie-uitgaven (ROAS) | Verkoopbedrag/advertentie-uitgaven | Valuta | (ROI) Geeft de verdiende dollars aan die aan de overeenkomstige reclame worden uitgegeven. |

## Rapporten configureren en uitvoeren

De laatste stap is de gegevensbronmetriek en om het even welke berekende metriek aan het Volgen rapport van de Code toe te voegen en neer in een campagne te boren om een directe mening van te krijgen hoe elke Advertentiegroep presteert.

1. Selecteer in **[!UICONTROL Adobe Analytics > Reports]** de rapportsuite waarin u gegevensbronnen hebt geïmporteerd.
1. Navigeer naar **[!UICONTROL Reports > Campaigns > Tracking Code > Tracking Code]** .
1. Selecteer het datumbereik.
1. Klik op **[!UICONTROL Metrics > Add]** en voeg de afmetingen van uw gegevensbron (klikken, Impressies, Totale kosten) toe uit de lijst Standaardstatistieken.
1. Doe het zelfde voor om het even welke berekende metriek u kunt hebben toegevoegd. Het rapport wordt bijgewerkt terwijl u metriek toevoegt.
