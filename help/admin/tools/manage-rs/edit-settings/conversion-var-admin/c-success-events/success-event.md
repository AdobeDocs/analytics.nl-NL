---
description: Gebeurtenissen met succes zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.
keywords: event
title: Overzicht van succesgebeurtenissen
feature: Metrics
role: Admin
exl-id: d52a691a-8124-4601-932f-d6d2d0a7842b
source-git-commit: ca84a5f807545d7196e2e0e90d3209c32d3fd789
workflow-type: tm+mt
source-wordcount: '924'
ht-degree: 1%

---

# Gebeurtenissen met succes

Gebeurtenissen met succes (ook wel conversiegebeurtenissen of aangepaste gebeurtenissen genoemd) zijn handelingen die kunnen worden bijgehouden. U bepaalt wat een succesgebeurtenis is. Als een bezoeker bijvoorbeeld een item aanschaft, kan de aankoopgebeurtenis als de succesgebeurtenis worden beschouwd.

Voor een videooverzicht van succesgebeurtenissen, zie [&#x200B; Inleiding aan omzettingsgebeurtenissen &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/analysis-workspace/metrics/introduction-to-conversion-events) in de gids van de Zelfstudies van de Analyse.

## Voorbeelden van succesgebeurtenissen

Afhankelijk van het type website zijn er vele soorten succesgebeurtenissen. Enkele voorbeelden:

* **Detailhandel**: De mening van het product, controle, aankoop
* **Media**: Abonnement, prijsteken-up, paginamening, videomening
* **Financiën**: De voorlegging van de toepassing, login, het gebruik van zelfbediening hulpmiddelen
* **Reizen**: Het boek (aankoop), interne campagne (klik-door), onderzoek (het tarief route)
* **Telecommunicatie**: De aankoop, leidt, het gebruik van zelfbedieningshulpmiddelen
* **Hoog Tech**: De download van het Witboek, RFP, vormvoltooiing, steunverzoeken
* **Automobielindustrie**: De voorlegger, verzoekt om een citaat, brochure download

De {[&#x200B; variabele 0} s.events bepaalt een succesgebeurtenis.](/help/implement/vars/page-vars/events/event-serialization.md)

## Succesgebeurtenissen configureren

U kunt de gebeurtenisvariabelen vormen die op uw plaats worden gebruikt. U kunt maximaal 1.000 succesgebeurtenissen toevoegen. De gebeurtenissen 81-1.000 werken slechts als u op code H22 of hoger bent.

Succesgebeurtenissen configureren:

1. Selecteer in Adobe Analytics **[!UICONTROL Admin]** > **[!UICONTROL Report Suites]** .
1. Selecteer de rapportsuite waar u succesgebeurtenissen wilt configureren.
1. Selecteer **[!UICONTROL Edit Settings]** > **[!UICONTROL Conversion]** > **[!UICONTROL Success Events]** .

   ![Stap Resultaat](/help/admin/tools/manage-rs/edit-settings/conversion-var-admin/c-success-events/assets/success_event_page.png)

1. In de [!UICONTROL **kolom van de Gebeurtenis**], identificeer de naam van de gebeurtenis die u als succesgebeurtenis wilt gebruiken.

1. Selecteer in de kolom **[!UICONTROL Name]** het selectievakje naast het item dat u wilt bewerken, en geef vervolgens de gewenste naam op.

   Geef belangrijke namen voor succesgebeurtenissen die op uw site worden gebruikt. Bijvoorbeeld, als event1 wordt gebruikt om registraties te volgen, verander hier de naam zodat event1 als metrische &quot;Registraties&quot;in alle rapporten van de Omzetting zal worden vertegenwoordigd.

1. Selecteer in de kolom **[!UICONTROL Type]** het selectievakje naast het item om de vervolgkeuzelijst in te schakelen en selecteer het gewenste type.

   >[!IMPORTANT]
   >
   >Houd rekening met het volgende wanneer u het gebeurtenistype wijzigt:<ul><li>U kunt het gebeurtenistype tussen teller en numeriek veranderen zonder toegang tot eerder gevangen gegevens te verliezen.</li><li>Wanneer u gebeurtenistypen wijzigt in of van een valutagebeurtenis, wordt een bericht weergegeven met de mededeling dat historische gegevens niet beschikbaar zijn in de rapportage. Verschillende gebeurtenistypen gebruiken afzonderlijke gegevenstabellen en kunnen niet gelijktijdig worden gebruikt. Sommige historische gegevens kunnen worden hersteld als de gebruiker het gebeurtenistype terugkeert. Gegevens die na de oorspronkelijke wijziging zijn verzameld, zijn echter niet beschikbaar.</li></ul>

   Het type dat u selecteert, bepaalt of de gebeurtenis een teller (standaard), numerieke, of muntgebeurtenis is. <p>Er worden tegengebeurtenissen gebruikt om een gebeurtenis in de tijd op te nemen.</p><p>Numerieke gebeurtenissen worden gebruikt voor het rapporteren van niet-valutagetallen, zoals het aantal coupons dat in een bestelling wordt gebruikt.</p> <p>Bij valutagebeurtenissen wordt een decimaal getal vastgelegd, zoals BTW of verzendkosten. De waarde die wordt doorgegeven aan valutatgebeurtenissen, wordt na ontvangst omgezet van de paginasaluta naar de basisvaluta van de rapportsuite. Valutapenheden worden gebruikt voor het bijhouden van belasting- en verzendkosten. Neem contact op met een Adobe-vertegenwoordiger voor meer informatie over het gebruik van valutagebeurtenissen.<p>Met numerieke gebeurtenissen en valutagebeurten kunt u metriek met meer dan één verhogen.</p><p>Gebeurtenissen die in het standaardtype van Gegevensbronnen worden gebruikt moeten numerieke of valutagebeurtenissen zijn.</p>

1. Selecteer in de kolom **[!UICONTROL Polarity]** het selectievakje en kies in het keuzemenu of een opwaartse trend voor deze metrische waarde goed of slecht is.

   op deze manier kunt u aangeven of Adobe Analytics het als goed of slecht moet beschouwen als een bepaalde aangepaste gebeurtenis (metrisch) wordt verhoogd. Het activeert richtingsindicatoren (pijlen) voor diverse metriek om context (bijvoorbeeld, week over week vergelijkingen) toe te voegen.  Voorbeelden: als &#39;Bugs Submit&#39; week in week uit gaat, moet Adobe Analytics dat dan als goed of slecht beschouwen? Een toename in e-mailregistraties is waarschijnlijk goed. Maar een toename in de fouten bij het verzenden van formulieren is waarschijnlijk slecht.  In Analysis Workspace wordt de polariteit toegepast op: Voorwaardelijke opmaak van de tabel voor vrije vorm, Overzichtswijzigingen en het kleurenschema Positief/Negatief van de visualisatie voor Kaart.

1. Selecteer in de kolom **[!UICONTROL Visibility]** het selectievakje en kies vervolgens in het keuzemenu of u de standaardmetriek (ingebouwde metriek), aangepaste gebeurtenissen en ingebouwde gebeurtenissen in het menu, Metrische kiezers, Berekende metrieke Builder en de Segmentbouwer wilt verbergen.

   Deze instelling heeft geen invloed op de gegevensverzameling voor die metrische waarde of gebeurtenis; deze instelling heeft alleen invloed op de zichtbaarheid in de gebruikersinterface, als volgt:

   De volgende instellingen zijn beschikbaar:

   | Instelling | Zichtbaar in | Niet zichtbaar in |
   |---------|----------|---------|
   | [!UICONTROL **Zichtbaar overal**] | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Berekende metrische bouwer</li></ul> | N.v.t. |
   | [!UICONTROL **Bouwvakkers**] | <ul><li>Segment Builder</li><li>Berekende metrische bouwer</li><li>Analysis Workspace</li></ul> |  |
   | [!UICONTROL **overal verborgen**] | N.v.t. | <ul><li>Analysis Workspace</li><li>Segment Builder</li><li>Berekende metrische bouwer</li></ul> |

1. In de [!UICONTROL **kolom van de Beschrijving**], selecteer checkbox, dan verstrek een beschrijving.
1. In de [!UICONTROL **Unieke kolom van de Opname van de Gebeurtenis**], selecteer checkbox, dan kies van het drop-down menu of om de gebeurtenis altijd te registreren.

   De volgende opties zijn beschikbaar:

   | Optie | Functie |
   |---------|----------|
   | [!UICONTROL **Verslag eens per Bezoek**] | Hiermee wordt de opgegeven gebeurtenis gekoppeld aan de bezoekerssessie. Volgende tellingen voor een bepaalde gebeurtenis tijdens hetzelfde bezoek worden genegeerd. Voor dit type gebeurtenisserialisatie zijn geen implementatiewijzigingen vereist. |
   | [!UICONTROL **identiteitskaart van de Gebeurtenis van het Gebruik**] | Koppelt de opgegeven gebeurtenis aan een aangepaste id. Volgende tellingen naar een bepaalde gebeurtenis met dezelfde gebeurtenis-id worden genegeerd. Voor dit type serienummering van gebeurtenissen is een aangepaste id vereist bij treffers om waarden te dedupliceren. Zie [&#x200B; identiteitskaart van de Gebeurtenis rangschikken &#x200B;](/help/implement/vars/page-vars/events/event-serialization.md) in de de gebruikersgids van het Uitvoeren. |

1. In de [!UICONTROL **kolom van de Deelname**], selecteer checkbox, dan kies of om participatie toe te laten of onbruikbaar te maken. Als deze optie is ingeschakeld, krijgt alle dimensie-items in het bezoek een volledige toewijzing.

   >[!NOTE]
   >
   >U kunt deelname inschakelen voor maximaal 100 aangepaste gebeurtenissen. Buiten dat, kunt u deelnemingsmetriek in de [&#x200B; Berekende Metriek &#x200B;](/help/components/calculated-metrics/workflow/c-build-metrics/participation-metric.md) bouwer tot stand brengen.

1. Selecteer **[!UICONTROL Save]**.
