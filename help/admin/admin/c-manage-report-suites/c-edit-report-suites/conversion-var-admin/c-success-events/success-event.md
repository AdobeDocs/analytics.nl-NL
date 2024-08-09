---
description: Gebeurtenissen met succes zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.
keywords: event
title: Overzicht van succesgebeurtenissen
feature: Event
role: Admin
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
source-git-commit: 38478fbccf7680e5b404b306136594e627d09a08
workflow-type: tm+mt
source-wordcount: '1334'
ht-degree: 1%

---

# Gebeurtenissen met succes

Gebeurtenissen met succes (ook wel conversiegebeurtenissen of aangepaste gebeurtenissen genoemd) zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.

Hier volgt een video-overzicht:

>[!VIDEO](https://video.tv.adobe.com/v/28764/?quality=12)

## Succesgebeurtenissen begrijpen

Afhankelijk van het type website zijn er vele soorten succesgebeurtenissen. Enkele voorbeelden:

* **Detailhandel**: De mening van het product, controle, aankoop
* **Media**: Abonnement, prijsteken-up, paginamening, videomening
* **Financiën**: De voorlegging van de toepassing, login, het gebruik van zelfbediening hulpmiddelen
* **Reizen**: Het boek (aankoop), interne campagne (klik-door), onderzoek (het tarief route)
* **Telecommunicatie**: De aankoop, leidt, het gebruik van zelfbedieningshulpmiddelen
* **Hoog Tech**: De download van het Witboek, RFP, vormvoltooiing, steunverzoeken
* **Automobielindustrie**: De voorlegger, verzoekt om een citaat, brochure download

De {](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/events/event-serialization.html) variabele 0} s.events bepaalt een succesgebeurtenis.[

## Succesgebeurtenissen configureren

U kunt de gebeurtenisvariabelen vormen die op uw plaats worden gebruikt. U kunt maximaal 1.000 succesgebeurtenissen toevoegen. De gebeurtenissen 81-1.000 werken slechts als u op code H22 of hoger bent.

Succesgebeurtenissen configureren:

1. Selecteer in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** .
1. Selecteer de rapportsuite waar u succesgebeurtenissen wilt configureren.
1. Selecteer **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Success Events]** .

   ![Stap Resultaat](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. In de [!UICONTROL **kolom van de Gebeurtenis**], identificeer de naam van de gebeurtenis die u als succesgebeurtenis wilt gebruiken.

1. Selecteer in de kolom **[!UICONTROL Name]** het selectievakje naast het item dat u wilt bewerken, en geef vervolgens de gewenste naam op.

   Geef belangrijke namen voor succesgebeurtenissen die op uw site worden gebruikt. Bijvoorbeeld, als event1 wordt gebruikt om registraties te volgen, verander hier de naam zodat event1 als metrische &quot;Registraties&quot;in alle rapporten van de Omzetting zal worden vertegenwoordigd.

1. Selecteer in de kolom **[!UICONTROL Type]** het selectievakje naast het item om de vervolgkeuzelijst in te schakelen en selecteer het gewenste type.

   >[!NOTE]
   >
   >U kunt een gebeurtenis wijzigen van een teller, een numerieke waarde of een valuta in een ander type zonder de toegang tot eerder vastgelegde gegevens te verliezen.

   Het type dat u selecteert, bepaalt of de gebeurtenis een teller (standaard), numerieke, of muntgebeurtenis is. <p>Er worden tegengebeurtenissen gebruikt om een gebeurtenis in de tijd op te nemen.</p><p>Numerieke gebeurtenissen worden gebruikt voor het rapporteren van niet-valutagetallen, zoals het aantal coupons dat in een bestelling wordt gebruikt.</p> <p>Bij valutagebeurtenissen wordt een decimaal getal vastgelegd, zoals BTW of verzendkosten. De waarde die wordt doorgegeven aan valutatgebeurtenissen, wordt na ontvangst omgezet van de paginasaluta naar de basisvaluta van de rapportsuite. Valutapenheden worden gebruikt voor het bijhouden van belasting- en verzendkosten. Neem contact op met een Adobe voor meer informatie over het gebruik van valutagebeurtenissen.<p>Met numerieke gebeurtenissen en valutagebeurten kunt u metriek met meer dan één verhogen.</p><p>Gebeurtenissen die in het standaardtype van Gegevensbronnen worden gebruikt moeten numerieke of valutagebeurtenissen zijn.</p>

1. Selecteer in de kolom **[!UICONTROL Polarity]** het selectievakje en kies in het keuzemenu of een opwaartse trend voor deze metrische waarde goed of slecht is.

   op deze manier kunt u aangeven of Adobe Analytics het als goed of slecht moet beschouwen als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd. Het activeert richtingsindicatoren (pijlen) voor diverse metriek om context (bijvoorbeeld, week over week vergelijkingen) toe te voegen.  Voorbeelden: als &#39;Bugs Submit&#39; week in week uit gaat, moet Adobe Analytics dat dan als goed of slecht beschouwen? Een toename in e-mailregistraties is waarschijnlijk goed. Maar een toename in de fouten bij het verzenden van formulieren is waarschijnlijk slecht.  In Analysis Workspace wordt de polariteit toegepast op: Voorwaardelijke opmaak van de tabel voor vrije vorm, Overzichtswijzigingen en het kleurenschema Positief/Negatief van de visualisatie voor Kaart.

1. Selecteer in de kolom **[!UICONTROL Visibility]** het selectievakje en kies vervolgens in het keuzemenu of u de standaardmetriek (ingebouwde metriek), aangepaste gebeurtenissen en ingebouwde gebeurtenissen in het menu, Metrische kiezers, Berekende metrieke Builder en de Segmentbouwer wilt verbergen.

   Deze instelling heeft geen invloed op de gegevensverzameling voor die metrische waarde of gebeurtenis; deze instelling heeft alleen invloed op de zichtbaarheid in de gebruikersinterface, als volgt:

   De volgende instellingen zijn beschikbaar:

   | Instelling | Zichtbaar in | Niet zichtbaar in |
   |---------|----------|---------|
   | [!UICONTROL **Zichtbaar overal**] | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Berekende metrische bouwer</li></ul> | N.v.t. |
   | [!UICONTROL **Bouwvakkers**] | <ul><li>Segment Builder</li><li>Berekende metrische bouwer</li><li>Analysis Workspace</li></ul> |
   | [!UICONTROL **overal verborgen**] | N.v.t. | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Berekende metrische bouwer</li></ul> |

1. In de [!UICONTROL **kolom van de Beschrijving**], selecteer checkbox, dan verstrek een beschrijving.
1. In de [!UICONTROL **Unieke kolom van de Opname van de Gebeurtenis**], selecteer checkbox, dan kies van het drop-down menu of om de gebeurtenis altijd te registreren.

   De volgende opties zijn beschikbaar:


| Optie | Functie |
|---------|----------|
| [!UICONTROL **Verslag eens per Bezoek**] | Hiermee wordt de opgegeven gebeurtenis gekoppeld aan de bezoekerssessie. Volgende tellingen voor een bepaalde gebeurtenis tijdens hetzelfde bezoek worden genegeerd. Voor dit type gebeurtenisserialisatie zijn geen implementatiewijzigingen vereist. |
| [!UICONTROL **identiteitskaart van de Gebeurtenis van het Gebruik**] | Koppelt de opgegeven gebeurtenis aan een aangepaste id. Volgende tellingen naar een bepaalde gebeurtenis met dezelfde gebeurtenis-id worden genegeerd. Voor dit type serienummering van gebeurtenissen is een aangepaste id vereist bij treffers om waarden te dedupliceren. Zie [ identiteitskaart van de Gebeurtenis rangschikken ](/help/implement/vars/page-vars/events/event-serialization.md) in de de gebruikersgids van het Uitvoeren. |

1. In de [!UICONTROL **kolom van de Deelname**], selecteer checkbox, dan kies of om participatie toe te laten of onbruikbaar te maken. Als deze optie is ingeschakeld, krijgt alle dimensie-items in het bezoek een volledige toewijzing.

   >[!NOTE]
   >
   >U kunt deelname inschakelen voor maximaal 100 aangepaste gebeurtenissen. Buiten dat, kunt u deelnemingsmetriek in de [ Berekende Metriek ](/help/components/c-calcmetrics/c-workflow/cm-workflow/c-build-metrics/participation-metric.md) bouwer tot stand brengen.

1. Selecteer **[!UICONTROL Save]** .

## Pagina Gebeurtenissen geslaagd - beschrijvingen {#section_681ECEC981694CABBDBF00E18165B447}

**[!UICONTROL Analytics]** > **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** > **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Success Events]**

Op de pagina Gebeurtenissen succes kunt u de gebeurtenisvariabelen configureren die op uw site worden gebruikt. U kunt maximaal 1.000 succesgebeurtenissen toevoegen. De gebeurtenissen 81-1.000 werken slechts als op code H22 of hoger.

| Element | Beschrijving |
|--- |--- |
| Gebeurtenis | De oorspronkelijke naam van de gebeurtenis. |
| Naam | Geef belangrijke namen voor succesgebeurtenissen die op uw site worden gebruikt. Bijvoorbeeld, als event1 wordt gebruikt om registraties te volgen, verander hier de naam zodat event1 als metrische &quot;Registraties&quot;in alle rapporten van de Omzetting zal worden vertegenwoordigd. |
| Type | Met het geselecteerde type bepaalt u of de gebeurtenis een teller (standaard), numerieke of valutagebeurtenis is. <p>Er worden tegengebeurtenissen gebruikt om een gebeurtenis in de tijd op te nemen.</p><p>Numerieke gebeurtenissen worden gebruikt voor het rapporteren van niet-valutagetallen, zoals het aantal coupons dat in een bestelling wordt gebruikt.</p> <p>Bij valutagebeurtenissen wordt een decimaal getal vastgelegd, zoals BTW of verzendkosten. De waarde die wordt doorgegeven aan valutatgebeurtenissen, wordt na ontvangst omgezet van de paginasaluta naar de basisvaluta van de rapportsuite. Valutapenheden worden gebruikt voor het bijhouden van belasting- en verzendkosten. Neem contact op met een Adobe voor meer informatie over het gebruik van valutagebeurtenissen.<p>Met numerieke gebeurtenissen en valutagebeurten kunt u metriek met meer dan één verhogen.</p><p>Gebeurtenissen die in het standaardtype van Gegevensbronnen worden gebruikt moeten numerieke of valutagebeurtenissen zijn.</p> |
| Polariteit | Met de metrische polariteit kunt u aangeven of Adobe Analytics het als goed of slecht moet beschouwen als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd. Hiermee kan Adobe Analytics richtingindicatoren (pijlen) weergeven voor verschillende metriek om context toe te voegen (bijvoorbeeld vergelijkingen van week tot week).  Voorbeelden: als &#39;Bugs Submit&#39; week in week uit gaat, moet Adobe Analytics dat dan als goed of slecht beschouwen? Een toename in e-mailregistraties is waarschijnlijk goed. Maar een toename in de fouten bij het verzenden van formulieren is waarschijnlijk slecht.  In Analysis Workspace wordt de polariteit toegepast op: Voorwaardelijke opmaak van de tabel voor vrije vorm, Overzichtswijzigingen en het kleurenschema Positief/Negatief van de visualisatie voor Kaart. |
| Beschrijving | Een korte beschrijving van het doel en het gebruik van de gebeurtenis. |
| Unieke gebeurtenisopname | **Verslag eens per Bezoek**: Banden de bepaalde gebeurtenis aan de zitting van de bezoeker. Volgende tellingen voor een bepaalde gebeurtenis tijdens hetzelfde bezoek worden genegeerd. Voor dit type gebeurtenisserialisatie zijn geen implementatiewijzigingen vereist.<br>**identiteitskaart van de Gebeurtenis van het Gebruik**: Banden de bepaalde gebeurtenis aan een douaneidentiteitskaart Volgende tellingen naar een bepaalde gebeurtenis met dezelfde gebeurtenis-id worden genegeerd. Voor dit type serienummering van gebeurtenissen is een aangepaste id vereist bij treffers om waarden te dedupliceren. Zie [ identiteitskaart van de Gebeurtenis rangschikken ](/help/implement/vars/page-vars/events/event-serialization.md) in de de gebruikersgids van het Uitvoeren. |
| Deelname | Geeft volledige toeschrijving aan alle dimensie-items in het bezoek. |
| Waarschuwing (valutagebeurtenis) | Wanneer u gebeurtenistypen wijzigt in of van een valutagebeurtenis, wordt een bericht weergegeven met de mededeling dat historische gegevens niet beschikbaar zijn in de rapportage.  Verschillende gebeurtenistypen gebruiken afzonderlijke gegevenstabellen en kunnen niet gelijktijdig worden gebruikt. Sommige historische gegevens kunnen worden hersteld als de gebruiker het gebeurtenistype terugkeert. Gegevens die na de oorspronkelijke wijziging zijn verzameld, zijn echter niet beschikbaar. Wees voorzichtig bij het wijzigen van een gebeurtenistype. |
