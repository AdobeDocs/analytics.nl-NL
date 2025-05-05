---
description: U kunt gegevens downloaden van Analysis Workspace door deze te kopiëren, of in de indelingen PDF en CSV.
title: PDF- of CSV-bestanden downloaden
feature: Curate and Share
role: User, Admin
exl-id: 085013dc-8263-4fc8-9492-99f0ecadf14b
source-git-commit: 04c588cbe8cd4cc9b8d6fe162e3623c2be076325
workflow-type: tm+mt
source-wordcount: '1014'
ht-degree: 0%

---

# PDF- of CSV-bestanden downloaden

Er zijn verschillende manieren om gegevens uit Analysis Workspace te exporteren. De methode die u kiest, is afhankelijk van de gegevensset die u wilt analyseren en van de vraag wie er toegang tot moet krijgen.

Geëxporteerde gegevens kunnen de vorm hebben van gekopieerde gegevens, CSV- of PDF-gegevens. Een PDF heeft doorgaans de voorkeur als u visualisaties in het bestand wilt opnemen. CSV en gekopieerde gegevens hebben de voorkeur als u gewoon gegevens zonder tekst wilt.

## Een project downloaden als CSV of PDF {#download-project}

Houd rekening met het volgende wanneer u projecten downloadt:

* Wanneer het downloaden van projecten als CSV of PDF, kan het project worden bewaard of unsaved wanneer u om een projectdownload verzoekt. Nochtans, slechts kunnen de bewaarde projecten [ gepland ](/help/analyze/analysis-workspace/curate-share/t-schedule-report.md) zijn.

* Bij het downloaden van projecten als een PDF:
   * Het exporteren van downloads kan enkele minuten in beslag nemen, omdat het project opnieuw wordt uitgevoerd op Adobe-servers voordat het wordt gerenderd in PDF-indeling. We raden u aan het project pas te laten nadat de PDF in uw browser is gedownload. U kunt echter wijzigingen in het project blijven aanbrengen terwijl u wacht. Als een PDF langer dan 5 minuten duurt om te renderen, wordt u gevraagd om het te e-mailen.
   * Downloads worden weergegeven als één pagina zonder paginering.
   * PDF-weergaven bevatten wat er op de pagina in Workspace staat. Als een project visualisaties en deelvensters van aangepaste grootte heeft, moet u deze wijzigen om automatisch van grootte te zijn (knop in de rechterbovenhoek), zodat er geen afgekapte inhoud is.
   * Om het even welke [ hyperlinks ](/help/analyze/analysis-workspace/visualizations/freeform-table/freeform-table-hyperlinks.md) die binnen vrije vormlijsten bestaan zijn niet functioneel in gedownloade PDF.

Een project downloaden als een CSV- of PDF-bestand:

1. Voer een van de volgende twee handelingen uit, afhankelijk van de indeling waarin u het project wilt downloaden:

   * **PDF:** Uitgezocht **[!UICONTROL Project]** > **[!UICONTROL Download PDF]**.

     Kies deze optie als het gedownloade bestand alle weergegeven (zichtbare) tabellen en visualisaties in het project moet bevatten.

   * **CSV:** Uitgezocht **[!UICONTROL Project]** > **[!UICONTROL Download CSV]**.

     Kies deze optie als u gegevens in onbewerkte tekst wilt.

   ![](assets/download-project.png)

1. (Voorwaardelijk) als u verkoos om een PDF te downloaden, wordt een bericht getoond nadat het project klaar is om te worden gedownload. Klik [!UICONTROL **Download**].
1. Klik op het pictogram **[!UICONTROL Download this file]** en sla het bestand op in een map naar keuze.

## Gegevens kopiëren naar klembord (sneltoets: Ctrl+C) {#copy-data}

Met de rechtermuisknop **[!UICONTROL Copy to clipboard]** kunt u snel gegevens van Workspace kopiëren en in een gereedschap van derden plakken.

* Als u de getoonde gekopieerde lijst wilt, klik de lijstkopbal met de rechtermuisknop aan en kies **gegevens van het Exemplaar aan klembord**.
* Als u een ondergroep van gekopieerde gegevens wilt, maak een selectie in de lijst en klik dan met de rechtermuisknop > **selectie van het Exemplaar aan klembord**.

>[!TIP]
>
>U kunt de sneltoets `Ctrl+C` gebruiken om de selectie naar het klembord te kopiëren en deze vervolgens met `Ctrl+V` in een gereedschap van derden te plakken.

![](assets/copy-selection.png)

## Gegevens downloaden als CSV {#download-data}

Met de rechtermuisknop klikken **[!UICONTROL Download data as CSV]** kunt u een gegevenslijst of de gegevensbron van een visualisatie als CSV downloaden.

* Klik met de rechtermuisknop en kies **[!UICONTROL Download data as CSV]** in de koptekst van een tabel of visualisatie. Dit downloadt de getoonde gegevens in de lijst of de onderliggende gegevensbron voor visualisatie als CSV.

  >[!NOTE]
  >
  >  Opmerking: deze optie wordt niet ondersteund door de Kaartweergave.

* Klik in een tabel met de rechtermuisknop en kies **[!UICONTROL Download selection as CSV]** . Alleen de selectie wordt met deze optie gedownload, in tegenstelling tot de volledige weergegeven tabel.

![](assets/download-data-viz.png)

## Items als CSV downloaden {#download-items}

Als u meer dan de zichtbare 400 rijen van gegevens in een lijst wilt analyseren, klik de lijstkopbal of om het even welke rij met de rechtermuisknop aan en selecteer **punten van de Download als CSV (_naam van het Dimension_)**. Met deze optie exporteert u maximaal 50.000 dimensieitems (op basis van de tabelsortering) voor de geselecteerde dimensie, met toegepaste filters en segmenten. Als u deze optie boven aan de tabel kiest, wordt de eerste afmeting in de tabel geëxporteerd. Hoewel er geen limieten gelden in de vrije-vormtabel, wordt aanbevolen de optie Items downloaden te gebruiken in tabellen met minder dan 20 kolommen om optimale prestaties te garanderen.

>[!TIP]
>
> Als uw afmeting groter is dan 50.000 items, downloadt u het bestand met verschillende maateenheden of past u een filter toe. U kunt bijvoorbeeld in één download aflopend sorteren op Bezoek en in een tweede download oplopend sorteren op Bezoek. Deze tip kan u helpen langer-staart punten terugwinnen.

U kunt meerdere taken uitvoeren in het project en zelfs naar een nieuw Workspace-project navigeren op hetzelfde tabblad terwijl het downloaden wordt uitgevoerd. Het downloaden wordt onderbroken als u een nieuw browsertabblad opent. Het downloaden wordt geannuleerd als u Workspace volledig verlaat of het browsertabblad sluit.

![](assets/download-items.png)

### Bestand met gedownloade items

De functies van de tabel worden als volgt op het gedownloade bestand toegepast:

* Alle deelvenstersegmenten worden als filters toegepast.
* De onderbrekingen **boven** de geselecteerde afmeting in de lijst worden toegepast als filters boven elke kolom.
* De onderbrekingen **onder** worden de geselecteerde afmeting in de lijst verwijderd.

In het bovenstaande voorbeeld worden pagina-items gedownload met het deelvenstersegment (Nieuwe bezoekers) en de bovenstaande componenten (Marketing Channel = e-mail) toegepast als filters, en worden de onderliggende componenten (Type mobiel apparaat) verwijderd uit de gedownloade CSV.

![](assets/downloaded-file.png)

### Meldingen downloaden

Terwijl het bestand wordt gedownload, wordt een informatieve melding over de voortgang weergegeven. U kunt de download op elk gewenst moment annuleren door op **[!UICONTROL Cancel download]** te klikken. Het sluiten van toast **zal niet** de download annuleren.

Nadat het bestand is voltooid, wordt een voltooiingsbericht weergegeven en wordt het bestand naar uw browser gedownload.

Als u meer dan één download tegelijk aanvraagt, ontvangt u een melding dat elke extra download in de wachtrij wordt geplaatst totdat de vorige download is voltooid.

![](assets/toast.png)

## Veelgestelde vragen {#faq}

| Vraag | Antwoord |
| --- | --- |
| Waarom is mijn gedownloade PDF één pagina? | Workspace pagineert momenteel geen gedownloade PDF. |
| Kan ik meer dan 50.000 items exporteren met de optie Items downloaden als CSV? | Terwijl elke download tot 50.000 afmetingspunten kan bevatten, kunt u het soort van uw lijst veranderen om langere eindpunten terug te winnen, of een filter toepassen om specifiekere punten te downloaden. |
| Wat doet **[!UICONTROL Copy visualization]**? | In tegenstelling tot [!UICONTROL **gegevens van het Exemplaar aan klembord**] of [!UICONTROL **selectie van het Exemplaar aan klembord**], is de **[!UICONTROL Copy visualization]** met de rechtermuisknop aanklikken optie geen uitvoeroptie. Hiermee kunt u een visualisatie of een deelvenster van de ene plaats in Workspace naar de andere kopiëren. Bijvoorbeeld van het ene naar het andere deelvenster in hetzelfde project of van het ene naar het andere project. [ intra-linking video ](https://experienceleague.adobe.com/docs/analytics-learn/tutorials/analysis-workspace/visualizations/intra-linking-in-analysis-workspace.html?lang=nl-NL) |
