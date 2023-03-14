---
title: Report Builder Veelgestelde vragen
description: Veelgestelde vragen over Report Builder.
feature: Report Builder
role: User, Admin
exl-id: 86604d39-2965-45a5-98ab-3ee4adcb7f97
source-git-commit: 51cac193cd2c88898139e079816a084c211a64f4
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# Report Builder Veelgestelde vragen

Veelgestelde vragen over Report Builder.

## Kan ik de `TODAY()` of `DATERANGE()` functioneren in werkboeken?

De [`TODAY()` function](https://support.microsoft.com/en-us/office/today-function-5eb3078d-a82c-4736-8930-2f51a028fdd9) in Excel retourneert de huidige dag. De [`DATEVALUE()` function](https://support.microsoft.com/en-us/office/datevalue-function-df8b07d4-7761-4a93-bc33-b7471bbff252) converteert een datumtekenreeks naar een seriële waarde. Hoewel nuttig voor vele eigenschappen binnen Excel, adviseert Adobe sterk tegen het gebruiken van deze functies als deel van Report Builder geplande verzoeken. De klantenservice van Adobe ondersteunt geen verzoeken om probleemoplossing met een van deze functies.

De geplande rapporten worden verwerkt op servers die waarschijnlijk geen tijdstreken als rapportreeks delen. De `TODAY()` een gebruiker verwacht en `TODAY()` het gebruik van de verwerkingsserver kan vaak anders zijn. De gebruikte datum is ook gebaseerd op het tijdstip waarop de verwerking start. Als veel rapporten tegelijkertijd worden uitgevoerd, kan de datum veranderen tussen de tijd het wordt gevraagd en wanneer het verwerking wegens vertragingen begint. Deze kwestie is aanwezig als de geplande tijd dicht bij middernacht is.

Geplande rapporten worden ook verwerkt op servers die waarschijnlijk geen datumsyntaxis delen. Bijvoorbeeld: `7/1/YYYY` kan naar 1 juli of 7 januari verwijzen, afhankelijk van uw land of regio. Met de `DATEVALUE()` op deze datum zou resulteren in verschillende seriële waarden, afhankelijk van de computer die het uitvoert.

Als alternatief voor het gebruiken van deze functies van Excel, adviseert Adobe hoogst gebruikend datumwaaiers binnen Report Builder verzoeken. Selecteer op de eerste pagina van de wizard Aanvragen de optie **[!UICONTROL Preset Dates]** in het vervolgkeuzemenu selecteert u vervolgens onder veelgebruikte datums de optie **[!UICONTROL Today]** of een ander gewenst datumbereik. Deze instelling neemt de tijd van de rapportsuite in beslag op het moment dat deze werd uitgevoerd, en niet op het moment dat de server de aanvraag verwerkt.

## Hoe groot en complex kan ik mijn werkboeken maken?

Report Builder ondersteunt werkboeken tot de volgende limieten:

* **1000 verzoeken**: Één enkel werkboek kan tot 1000 gegevensverzoeken bevatten. Als u rapporten of projecten hebt die meer dan 1000 verzoeken vereisen, adviseert Adobe om hen te scheiden in veelvoudige werkboeken.
* **20.000 aanvragen per uur per bedrijf**: Report Builder gebruikt de API voor analyserapportage om gegevens op te halen. Elke individuele aanvraag gebruikt een API-aanroep wanneer deze wordt gemaakt of vernieuwd. Als uw organisatie meer dan 20.000 API vraag in een bepaald uur accumuleert, moet u tot het volgende uur wachten om gegevens opnieuw terug te winnen.
* **Verwerkingsduur van 4 uur**: De geplande tijd van rapporten uit na verwerking meer dan 4 uren. Als uw werkboek vele complexe verzoeken gebruikend grote gegevensreeksen bevat, kan het geplande rapport ontbreken.
