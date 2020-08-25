---
description: U kunt gegevens downloaden van Analysis Workspace door deze te kopiëren of in PDF- en CSV-indeling.
title: PDF- of CSV-bestanden downloaden
uuid: 8af5f3d7-5870-4ed6-8a9f-ef290a48ef5f
translation-type: tm+mt
source-git-commit: ab5d2be12100306410486fea31bacc6ee9756738
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 1%

---


# PDF- of CSV-bestanden downloaden vanuit Workspace

Er zijn verschillende manieren waarop u gegevens uit Analysis Workspace kunt exporteren, afhankelijk van de gegevensset die u buiten het hulpprogramma wilt analyseren en van de vraag wie de gegevens moet ontvangen. Geëxporteerde gegevens kunnen de vorm hebben van gekopieerde gegevens, CSV- of PDF-bestanden. Een PDF heeft doorgaans de voorkeur als u visualisaties in het bestand wilt opnemen, terwijl een CSV (of gekopieerde gegevens) de voorkeur heeft als u gewoon gegevens zonder opmaak wilt.

>[!IMPORTANT]
>
> Sommige opties waarnaar op deze pagina wordt verwezen, zoals **Items downloaden als CSV**, worden momenteel beperkt getest. [Meer informatie](https://docs.adobe.com/content/help/nl-NL/analytics/landing/an-releases.html)

## Project downloaden als CSV of PDF {#download-project}

U kunt een volledig project downloaden door naar Project > **Downloaden als PDF (of als CSV)** te gaan. Het gedownloade bestand bevat alle weergegeven (zichtbare) tabellen en visualisaties in het project. Een PDF heeft doorgaans de voorkeur als u visualisaties in het bestand wilt opnemen, terwijl een CSV-bestand de voorkeur heeft als u gewoon gegevens met normale tekst wilt.

Houd bij het downloaden van projecten rekening met:

* Het project kan worden opgeslagen of niet opgeslagen wanneer u een projectdownload aanvraagt. Nochtans, slechts kunnen de bewaarde projecten worden [gepland](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/curate-share/t-schedule-report.html).
* PDF-bestanden die in de browser worden gedownload, kunnen enkele minuten duren om te worden geëxporteerd, omdat het project opnieuw op Adobe-servers wordt uitgevoerd voordat het in PDF-indeling wordt gerenderd. We raden u aan het project pas te laten nadat de PDF in uw browser is gedownload. U kunt echter wijzigingen in het project blijven aanbrengen terwijl u wacht. Als een PDF langer dan 5 minuten duurt om te worden gerenderd, wordt u gevraagd om deze te e-mailen.
* PDF-downloads worden weergegeven als één pagina zonder paginering.
* Wanneer een project naar PDF wordt gerenderd, geven wij terug wat op de pagina is. Als een project visualisaties en deelvensters van aangepaste grootte heeft, moet u deze wijzigen om automatisch van grootte te zijn (knop in de rechterbovenhoek), zodat er geen afgekapte inhoud is.

## Gegevens kopiëren naar klembord (hotkey: Ctrl+C) {#copy-data}

Klik met de rechtermuisknop > Kopiëren naar klembordopties om gegevens snel te kopiëren uit Workspace en te plakken naar een andere locatie.

* Als u de weergegeven tabel wilt kopiëren, klikt u met de rechtermuisknop op de tabelkop en kiest u Weergegeven gegevens **kopiëren naar klembord**.
* Als u een subset van gegevens wilt kopiëren, maakt u een selectie in de tabel en klikt u met de rechtermuisknop > Selectie **kopiëren naar klembord**.

Daarnaast wordt de selectie via de sneltoets **Ctrl+C** naar het klembord gekopieerd. Nadat u de gegevens hebt gekopieerd, kunt u naar een ander gereedschap gaan en deze plakken (of op Ctrl+V drukken).

## Gegevens downloaden als CSV {#download-data}

Klik met de rechtermuisknop > Downloaden als CSV-opties om een gegevenslijst of de gegevensbron van een visualisatie als CSV te downloaden.

* Klik in de koptekst van een tabel met de rechtermuisknop > Weergegeven gegevens **downloaden als CSV**. Hiermee worden de weergegeven gegevens in de tabel gedownload als een CSV-bestand.
* Als een selectie in de tabel wordt gemaakt, staat de optie Selectie **downloaden als CSV**. Alleen de selectie wordt met deze optie gedownload, in tegenstelling tot de volledige weergegeven tabel.
* Klik in de kop van een visualisatie met de rechtermuisknop > **Gegevens downloaden als CSV**. Hiermee wordt de gegevensbrontabel gedownload voor visualisatie als een CSV-bestand. Opmerking: Deze optie wordt niet ondersteund door de Kaartweergave.

## Items als CSV downloaden {#download-items}

Als u meer dan de zichtbare 400 rijen gegevens in een lijst wilt analyseren, klik de lijstkopbal of om het even welke rij met de rechtermuisknop aan en selecteer punten van de **Download als CSV (naam van Dimension)**. Met deze optie kunt u maximaal 50.000 dimensiepunten exporteren voor de geselecteerde dimensie (op basis van de tabelsortering), met toegepaste filters en segmenten. Als u deze optie boven aan de tabel kiest, wordt de eerste afmeting in de tabel geëxporteerd. Hoewel er geen limieten gelden in de vrije-vormtabel, wordt aanbevolen de optie Items downloaden te gebruiken in tabellen met minder dan 20 kolommen om optimale prestaties te garanderen.

>[!TIP]
>
> Als uw afmeting groter is dan 50.000 items, downloadt u het bestand met verschillende maateenheden of past u een filter toe. U kunt bijvoorbeeld in één download aflopend sorteren op Bezoek en in een tweede download oplopend sorteren op Bezoek. Deze tip kan u helpen langer-staart punten terugwinnen.

U kunt meerdere taken uitvoeren binnen het project en zelfs naar een nieuw Workspace-project navigeren op hetzelfde tabblad terwijl de download bezig is. Het downloaden wordt onderbroken als u een nieuw browsertabblad opent. Het downloaden wordt geannuleerd als u Workspace volledig verlaat of het browsertabblad sluit.

### Bestand met gedownloade items

De functies van de tabel worden als volgt op het gedownloade bestand toegepast:

* Alle deelvenstersegmenten worden als filters toegepast.
* Onderverdelingen **boven** de geselecteerde dimensie in de tabel worden toegepast als filters boven elke kolom.
* Onderverdelingen **onder** de geselecteerde dimensie in de tabel worden verwijderd.

In het bovenstaande voorbeeld worden pagina-items gedownload met het deelvenstersegment (Klanten van nieuwe bezoekers) en de bovenstaande componenten (Marketing Channel = e-mail) die als filters zijn toegepast, en worden de onderliggende componenten (Type mobiel apparaat) verwijderd uit de gedownloade CSV.

### Meldingen downloaden

Terwijl het bestand wordt gedownload, wordt een informatieve melding over de voortgang weergegeven. U kunt de download op elk gewenst moment annuleren door op Downloaden annuleren te klikken. Als u de pop sluit, **wordt het downloaden niet** geannuleerd.

Nadat het bestand is voltooid, wordt een voltooiingsbericht weergegeven en wordt het bestand naar uw browser gedownload.

Als u meer dan één download tegelijk aanvraagt, ontvangt u een melding dat elke extra download in de wachtrij wordt geplaatst totdat de vorige download is voltooid.

## Veelgestelde vragen {#faq}

| Vraag | Antwoord |
| --- | --- |
| Waarom is mijn gedownloade PDF één pagina? | De gedownloade PDF&#39;s worden momenteel niet door de werkruimte gepagineerd. |
| Kan ik meer dan 50.000 items exporteren met de optie Items downloaden als CSV? | Terwijl elke download tot 50.000 afmetingspunten kan bevatten, kunt u het soort van uw lijst veranderen om langere eindpunten terug te winnen, of een filter toepassen om specifiekere punten te downloaden. |
| Wat doet &#39;visualisatie kopiëren&#39;? | Visualisatie kopiëren is geen exportoptie. Hiermee kunt u een visualisatie of een deelvenster van de ene plaats in Workspace naar de andere kopiëren. Bijvoorbeeld, van één paneel aan een andere in het zelfde project, of van één project aan een ander project. [De video bekijken](https://www.youtube.com/watch?v=lvmAdKNfWQw) |

