---
description: Gebeurtenissen met succes zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.
keywords: event
title: Overzicht van succesgebeurtenissen
feature: Event
role: Admin
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
source-git-commit: 429aaa43fdae669350bdb5a5a54a7d4b9b1c65f2
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# Overzicht van succesgebeurtenissen

Gebeurtenissen met succes (ook wel conversiegebeurtenissen of aangepaste gebeurtenissen genoemd) zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/28764/?quality=12)

Open de pagina Gebeurtenissen succes in de montages van de rapportreeks:

1. Aanmelden bij [experiencecloud.adobe.com](https://experiencecloud.adobe.com) met uw Adobe-id-referenties.
2. Klik op de knop met het 9-raster bovenaan en klik vervolgens op [!UICONTROL Analytics].
3. Navigeren naar [!UICONTROL Admin] > [!UICONTROL Report Suites]
4. Selecteer de gewenste rapportsuite en navigeer naar [!UICONTROL Edit Settings] > [!UICONTROL Conversion] > [!UICONTROL Success Events].

Afhankelijk van het type website zijn er vele soorten succesgebeurtenissen. Enkele voorbeelden:

* **Detailhandel**: Productweergave, kassa, aankoop
* **Media**: Abonnement, prijsaanmelding, paginaweergave, videoweergave
* **Financiën**: Gebruik van toepassingen voor verzending, aanmelding en zelfbediening
* **Reizen**: Boek (aankoop), interne campagne (doorklikken), zoeken (prijsopgave)
* **Telecommunicatie**: Gebruik van tools voor aanschaf, leads en selfservice
* **Hoge technologie**: whitepaper downloaden, RFP, formuliervoltooiing, supportverzoeken
* **Automobielen**: verzenden van leads, aanvragen voor een offerte, downloaden van brochures

De [s.events](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html) de variabele definieert een succesgebeurtenis.

## Pagina Gebeurtenissen geslaagd - beschrijvingen {#section_681ECEC981694CABBDBF00E18165B447}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Success Events]**

Op de pagina Gebeurtenissen succes kunt u de gebeurtenisvariabelen configureren die op uw site worden gebruikt. U kunt maximaal 1.000 succesgebeurtenissen toevoegen. De gebeurtenissen 81-1.000 werken slechts als op code H22 of hoger.

| Element | Beschrijving |
|--- |--- |
| Gebeurtenis | De oorspronkelijke naam van de gebeurtenis. |
| Naam | Geef belangrijke namen voor succesgebeurtenissen die op uw site worden gebruikt. Bijvoorbeeld, als event1 wordt gebruikt om registraties te volgen, verander hier de naam zodat event1 als metrische &quot;Registraties&quot;in alle rapporten van de Omzetting zal worden vertegenwoordigd. |
| Type | Met het geselecteerde type bepaalt u of de gebeurtenis een teller (standaard), numerieke of valutagebeurtenis is. Met numerieke gebeurtenissen en valutagebeurten kunt u metriek met meer dan één verhogen.  Tegengebeurtenissen worden gebruikt om een gebeurtenis in de tijd op te nemen, terwijl valutagebeurtenissen een decimaal getal opnemen, zoals belastingen of verzendkosten. De waarde die wordt doorgegeven aan valutatgebeurtenissen, wordt na ontvangst omgezet van de paginasaluta naar de basisvaluta van de rapportsuite. Neem contact op met een Adobe voor meer informatie over het gebruik van valutagebeurtenissen. Numerieke gebeurtenissen worden gebruikt voor het rapporteren van niet-valutagetallen, zoals het aantal coupons dat in een bestelling wordt gebruikt. Valutapenheden worden gebruikt voor het bijhouden van belasting- en verzendkosten. Gebeurtenissen die in het standaardtype van Gegevensbronnen worden gebruikt moeten numerieke of valutagebeurtenissen zijn. |
| Polariteit | Met de metrische polariteit kunt u aangeven of Adobe Analytics het als goed of slecht moet beschouwen als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd. Hiermee kan Adobe Analytics richtingindicatoren (pijlen) weergeven voor verschillende metriek om context toe te voegen (bijvoorbeeld week-over-week vergelijkingen).  Voorbeelden: als &#39;Bugs Submit&#39; week in week uit gaat, moet Adobe Analytics dat dan als goed of slecht beschouwen? Een toename in e-mailregistraties is waarschijnlijk goed. Maar een toename in de fouten bij het verzenden van formulieren is waarschijnlijk slecht.  In Analysis Workspace wordt de polariteit toegepast op: Voorwaardelijke opmaak van de tabel voor vrije vorm, Overzichtswijzigingen en het kleurenschema Positief/Negatief van de visualisatie voor Kaart. |
| Beschrijving | Een korte beschrijving van het doel en het gebruik van de gebeurtenis. |
| Unieke gebeurtenisopname | **Eén keer opnemen per bezoek**: Koppelt de opgegeven gebeurtenis aan de bezoekerssessie. Volgende tellingen voor een bepaalde gebeurtenis tijdens hetzelfde bezoek worden genegeerd. Voor dit type gebeurtenisserialisatie zijn geen implementatiewijzigingen vereist.<br>**Gebeurtenis-id gebruiken**: Koppelt de opgegeven gebeurtenis aan een aangepaste id. Volgende tellingen naar een bepaalde gebeurtenis met dezelfde gebeurtenis-id worden genegeerd. Voor dit type serienummering van gebeurtenissen is een aangepaste id vereist bij treffers om waarden te dedupliceren. Zie [Serienummering voor gebeurtenis-id](/help/implement/vars/page-vars/events/event-serialization.md) in de gebruikershandleiding Implementeren. |
| Deelname | Geeft volledige toeschrijving aan alle dimensie-items in het bezoek. |
| Waarschuwing (valutagebeurtenis) | Wanneer u gebeurtenistypen wijzigt in of van een valutagebeurtenis, wordt een bericht weergegeven met de mededeling dat historische gegevens niet beschikbaar zijn in de rapportage.  Verschillende gebeurtenistypen gebruiken afzonderlijke gegevenstabellen en kunnen niet gelijktijdig worden gebruikt. Sommige historische gegevens kunnen worden hersteld als de gebruiker het gebeurtenistype terugkeert. Gegevens die na de oorspronkelijke wijziging zijn verzameld, zijn echter niet beschikbaar. Wees voorzichtig bij het wijzigen van een gebeurtenistype. |
