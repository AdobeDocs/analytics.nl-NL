---
description: Gebeurtenissen met succes zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.
keywords: event
title: Overzicht van succesgebeurtenissen
feature: Event
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
source-git-commit: d8603ddd6cee2ccc930281003d9ff1befa15c95c
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 2%

---

# Overzicht van succesgebeurtenissen

Gebeurtenissen met succes (ook wel conversiegebeurtenissen of aangepaste gebeurtenissen genoemd) zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/28764/?quality=12)

Open de pagina Gebeurtenissen succes in de montages van de rapportreeks:

1. Aanmelden bij [ExperienceCloud.adobe.com](https://experiencecloud.adobe.com) met uw Adobe-id-referenties.
2. Klik op de knop met het 9-raster bovenaan en klik vervolgens op [!UICONTROL Analytics].
3. Ga naar [!UICONTROL Admin] > [!UICONTROL Report Suites]
4. Selecteer de gewenste rapportsuite en navigeer naar [!UICONTROL Edit Settings] > [!UICONTROL Conversion] > [!UICONTROL Success Events].
5. Zoek de gewenste gebeurtenis en wijzig deze [!UICONTROL Unique Event Recording] vervolgkeuzelijst naar [!UICONTROL Record Once Per Visit] of [!UICONTROL Use Event ID].

Afhankelijk van het type website zijn er vele soorten succesgebeurtenissen. Enkele voorbeelden:

* **Detailhandel**: Productweergave, afrekenen, aanschaffen
* **Media**: Abonnement, prijsaanmelding, paginaweergave, videoweergave
* **Financiën**: Toepassingen verzenden, aanmelden, gebruik van tools voor zelfbediening
* **Reizen**: Boek (aankoop), interne campagne (doorklikken), onderzoek (prijsopgave)
* **Telecommunicatie**: Gebruik van tools voor kopen, leads en zelfbediening
* **Hoge technologie**: Whitepaper downloaden, RFP, formuliervoltooiing, supportaanvragen
* **Automobielindustrie**: Indiening van leads, aanvragen voor een prijsopgave, downloaden via brochure

De [s.events](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html) variable definieert een success event.

## Pagina Gebeurtenissen geslaagd - beschrijvingen {#section_681ECEC981694CABBDBF00E18165B447}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Success Events]**

Op de pagina Gebeurtenissen succes kunt u de gebeurtenisvariabelen configureren die op uw site worden gebruikt. U kunt maximaal 1.000 succesgebeurtenissen toevoegen. De gebeurtenissen 81-1.000 werken slechts als op code H22 of hoger.

| Element | Beschrijving |
|--- |--- |
| Gebeurtenis | De oorspronkelijke naam van de gebeurtenis. |
| Naam | Geef belangrijke namen voor succesgebeurtenissen die op uw site worden gebruikt. Bijvoorbeeld, als event1 wordt gebruikt om registraties te volgen, verander hier de naam zodat event1 als metrische &quot;Registraties&quot;in alle rapporten van de Omzetting zal worden vertegenwoordigd. |
| Type | Met het geselecteerde type bepaalt u of de gebeurtenis een teller (standaard), numerieke of valutagebeurtenis is. Met numerieke gebeurtenissen en valutagebeurten kunt u metriek met meer dan één verhogen.  Tegengebeurtenissen worden gebruikt om een gebeurtenis in de tijd op te nemen, terwijl valutagebeurten een decimaal getal opnemen, zoals belasting of verzending. De waarde die wordt doorgegeven aan valutatgebeurtenissen, wordt na ontvangst omgezet van de paginasaluta naar de basisvaluta van de rapportsuite. Neem contact op met een Adobe-medewerker voor meer informatie over het gebruik van valutagebeurtenissen. Numerieke gebeurtenissen worden gebruikt voor het rapporteren van niet-valutagetallen, zoals het aantal coupons dat in een bestelling wordt gebruikt. Valutapenheden worden gebruikt voor het bijhouden van belasting- en verzendkosten. Gebeurtenissen die in het standaardtype van Gegevensbronnen worden gebruikt moeten numerieke of valutagebeurtenissen zijn. |
| Polariteit | Met de metrische polariteit kunt u aangeven of Adobe Analytics het als goed of slecht moet beschouwen als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd. Hiermee kan Adobe Analytics richtingindicatoren (pijlen) weergeven voor verschillende metriek om context toe te voegen (bijvoorbeeld week-over-week vergelijkingen).  Voorbeelden: Als &quot;Ingediende bugs&quot; week in week uit gaat, moet Adobe Analytics dat dan als goed of slecht beschouwen? Een toename in e-mailregistraties is waarschijnlijk goed. Maar een toename in de fouten bij het verzenden van formulieren is waarschijnlijk slecht.  In Analysis Workspace wordt polariteit toegepast op: Voorwaardelijke opmaak van de tabel voor vrije vorm, visualisaties van Summiere wijzigingen en het kleurenschema Positief/Negatief van de visualisatie voor Kaarten. |
| Beschrijving | Een korte beschrijving van het doel en het gebruik van de gebeurtenis. |
| Unieke gebeurtenisopname | **Eén keer opnemen per bezoek**: Hiermee wordt de opgegeven gebeurtenis gekoppeld aan de sessie van de bezoeker. Volgende tellingen voor een bepaalde gebeurtenis tijdens hetzelfde bezoek worden genegeerd. Voor dit type gebeurtenisserialisatie zijn geen implementatiewijzigingen vereist.<br>**Gebeurtenis-id gebruiken**: Koppelt de opgegeven gebeurtenis aan een aangepaste id. Volgende tellingen naar een bepaalde gebeurtenis met dezelfde gebeurtenis-id worden genegeerd. Voor dit type serienummering van gebeurtenissen is een aangepaste id vereist bij treffers om waarden te dedupliceren. Zie [Serienummering voor gebeurtenis-id](../../../implement/vars/page-vars/events/event-serialization.md) in de gebruikershandleiding Implementeren. |
| Deelname | Geeft volledige toeschrijving aan alle dimensie-items in het bezoek. |
| Waarschuwing (valutagebeurtenis) | Wanneer u gebeurtenistypen wijzigt in of van een valutagebeurtenis, wordt een bericht weergegeven met de mededeling dat historische gegevens niet beschikbaar zijn in de rapportage.  Verschillende gebeurtenistypen gebruiken afzonderlijke gegevenstabellen en kunnen niet gelijktijdig worden gebruikt. Sommige historische gegevens kunnen worden hersteld als de gebruiker het gebeurtenistype terugkeert. Gegevens die na de oorspronkelijke wijziging zijn verzameld, zijn echter niet beschikbaar. Wees voorzichtig bij het wijzigen van een gebeurtenistype. |
