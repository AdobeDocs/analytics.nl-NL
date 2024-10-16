---
description: Meer informatie over vaak gestelde vragen over Report Builder.
title: Veelgestelde vragen over Report Builder
feature: Report Builder
role: User, Admin
exl-id: 86604d39-2965-45a5-98ab-3ee4adcb7f97
source-git-commit: bb908f8dd21f7f11d93eb2e3cc843f107b99950d
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Veelgestelde vragen over Report Builder

Veelgestelde vragen over Report Builder.

## Kan ik de functie `TODAY()` of `DATERANGE()` in werkboeken gebruiken? {#today}

De [`TODAY()` functie ](https://support.microsoft.com/en-us/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) in Excel keert de huidige dag terug. De [`DATEVALUE()` functie ](https://support.microsoft.com/en-us/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) zet een datumkoord in een periodieke waarde om. Hoewel nuttig voor vele eigenschappen binnen Excel, adviseert de Adobe sterk tegen het gebruiken van deze functies als deel van Report Builder geplande verzoeken. De Zorg van de Klant van de Adobe steunt geen het oplossen van problemenverzoeken gebruikend één van beiden van deze functies.

De geplande rapporten worden verwerkt op servers die waarschijnlijk geen tijdstreken als rapportreeks delen. De `TODAY()` die een gebruiker verwacht en de `TODAY()` die de verwerkingsserver gebruikt, kunnen vaak anders zijn. De gebruikte datum is ook gebaseerd op het tijdstip waarop de verwerking start. Als veel rapporten tegelijkertijd worden uitgevoerd, kan de datum veranderen tussen de tijd het wordt gevraagd en wanneer het verwerking wegens vertragingen begint. Deze kwestie is aanwezig als de geplande tijd dicht bij middernacht is.

Geplande rapporten worden ook verwerkt op servers die waarschijnlijk geen datumsyntaxis delen. `7/1/YYYY` kan bijvoorbeeld naar 1 juli of 7 januari verwijzen, afhankelijk van uw land of regio. Als u de functie `DATEVALUE()` op deze datum gebruikt, worden verschillende seriële waarden gebruikt, afhankelijk van de computer die de functie uitvoert.

Als alternatief voor het gebruiken van deze functies van Excel, adviseert de Adobe hoogst gebruikend datumwaaiers binnen Report Builder verzoeken. Selecteer op de eerste pagina van de aanvraagwizard **[!UICONTROL Preset Dates]** in de vervolgkeuzelijst en selecteer vervolgens onder Algemeen gebruikte datums **[!UICONTROL Today]** of een ander gewenst datumbereik. Deze instelling neemt de tijd van de rapportsuite in beslag op het moment dat deze werd uitgevoerd, en niet op het moment dat de server de aanvraag verwerkt.

## Hoe groot en complex kan ik mijn werkboeken maken? {#complexity}

Report Builder ondersteunt werkboeken tot de volgende limieten:

* **1000 verzoeken**: Één enkel werkboek kan tot 1000 gegevensverzoeken bevatten. Als u rapporten of projecten hebt die meer dan 1000 verzoeken vereisen, adviseert de Adobe hen te scheiden in veelvoudige werkboeken.
* **20K verzoeken per uur per bedrijf**: De Report Builder gebruikt Analytics die API melden om gegevens terug te winnen. Elke individuele aanvraag gebruikt een API-aanroep wanneer deze wordt gemaakt of vernieuwd. Als uw organisatie meer dan 20.000 API vraag in een bepaald uur accumuleert, moet u tot het volgende uur wachten om gegevens opnieuw terug te winnen.
* **4 uur verwerkingstijd**: Geplande rapporttijd uit na verwerking meer dan 4 uren. Als uw werkboek vele complexe verzoeken gebruikend grote gegevensreeksen bevat, kan het geplande rapport ontbreken.

## Hoe weet ik of ik toegang heb tot Report Builder? {#access}

Uw Adobe Analytics-beheerder moet toegang tot de Report Builder verlenen. Admin plaatst omhoog productprofielen in [ Adobe Admin Console ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-console/home). Vraag uw beheerder om u toegang te verlenen.
