---
description: De gemiddelden van vertoningen voor metriek in de Campagnes rapporterend groep. De standaardmetriek zijn klikthrough, Totale Verkoop, Orden, en Inkomsten.
title: Kampeerconversietrechter
topic: Reports
uuid: b0a90917-e4c7-40da-854e-58649de09742
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Kampeerconversietrechter

De gemiddelden van vertoningen voor metriek in de Campagnes rapporterend groep. De standaardmetriek zijn klikthrough, Totale Verkoop, Orden, en Inkomsten.

**[!UICONTROL Campaigns]** > **[!UICONTROL Campaign Conversion Funnel]**

Boven aan een trechter-afbeelding worden conversiegegevens weergegeven. De bodem toont statistieken voor alle gebeurtenissen in het hoogste gebied, die op Orden en tot twee andere metriek, Inkomsten en Eenheden worden gebaseerd.

Houd rekening met de volgende informatie bij het interpreteren van gegevens van conversietrechter:

* De statistieken voor huidige tijdperiodes zouden niet kunnen worden voltooid wanneer u gegevens bekijkt, die trends van een vorige dag aan huidige kunnen beïnvloeden.
* Wanneer geen filter op de trechter wordt toegepast, toont metrisch Bezoek omzettingsbezoeken, of bezoeken waarin de campagnevariabele, om het even welke eVar variabele, of een succesgebeurtenis werd in brand gestoken. Bezoeken waarbij geen van deze eigenschappen in rapporten is doorgegeven, worden niet in dit totaal opgenomen.
* Wanneer een filter op de trechter wordt toegepast, metrisch van Bezoek instanties (of klik-door) vertegenwoordigt. Deze waarde is het totale aantal keren dat de gegeven variabele door gebruikers op uw plaats werd bevolkt, exclusief die instanties die niet aan de filtervereisten voldoen. Bij één bezoek kunnen meerdere instanties betrokken zijn.
* Het is mogelijk dat hogere niveaus in de trechter hogere aantallen dan ontoelaatbare niveaus rapporteren. U ziet bijvoorbeeld meer bestellingen dan doorklikken of meer kassa&#39;s dan productweergaven. Er zijn een aantal redenen waarom deze situatie zich voordoet:

   * U hebt meer orden dan klik-door als de het Volgen variabele van de Code aan een lange koekjesafloop (bijvoorbeeld, een maand) wordt geplaatst, en de gebruikers voeren slechts één klik-door maar keren verscheidene tijden terug en plaatsen orden tijdens de periode, alvorens de het Volgen waarde van de Code verloopt.
   * U hebt meer kassa&#39;s dan productweergaven als de gebruiker de pagina met de productweergave kan overslaan (zoals in het geval van een pagina voor uploaden) of als de gebruiker zijn winkelwagentje kan opslaan en later kan terugkeren om de bestelling te voltooien. Als de productweergave plaatsvindt voordat het geselecteerde datumbereik is bereikt en het uitchecken daarna plaatsvindt, ziet u één uitcheckweergave en geen productweergaven. Als u een dergelijke discrepantie opmerkt, geeft dit geen probleem aan met de rapportage of zelfs niet met een implementatiefout. In plaats daarvan kunt u deze gegevens gebruiken om te begrijpen hoe gebruikers met uw site communiceren, zelfs als de trechter niet op de verwachte manier past.

