---
title: Apparaatanalyse
description: Analytics voor verschillende apparaten wijzigt uw gegevens van apparaatfocus naar persoonlijke focus door apparaatgegevens aan elkaar te hechten.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Apparaatanalyse

>[!NOTE] De documentatie van de Analyse van verschillende apparaten kan worden gewijzigd aangezien de eigenschap verder wordt ontwikkeld. Controleer regelmatig of er updates zijn.

Apparaatanalyse is een functie waarmee analyses worden getransformeerd van een apparaatgecentreerde weergave naar een persoonlijke weergave. Deze functie gebruikt de Adobe Experience Platform Identity Service Co-op Graph of Private Graph om te bepalen welke apparaten bij personen horen en ze aan elkaar te koppelen. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. U kunt CDA gebruiken om vragen zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van campagnedoeltreffendheid als ik rekening houd met apparatuurreizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunnen opbrengsten worden toegeschreven aan de advertentie waarop ze op hun desktopcomputer hebben geklikt.

Zie [Reis IQ: De pagina](http://adobe.ly/aacda) van de Vonk van de Analyse van de Apparaten voor meer informatie over de mogelijkheden en de eigenschappen van de Analytics van het Apparaat.

## Vereisten

Vanaf september 2019 vereist Cross-Device Analytics het volgende. Werk met teams binnen uw organisatie en uw accountmanager van Adobe om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!IMPORTANT] Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* De gegevens van uw organisatie moeten zich in het datacenter van het Pacific Northwest van Adobe bevinden. Er is voorzien in steun voor datacentra in andere regio&#39;s van de wereld.
* Neem contact op met de accountmanager van uw organisatie om de volgende belangrijke punten vast te stellen:
   * Er moet een contract worden ondertekend met Adobe Analytics Ultimate.
   * Uw organisatie moet de Adobe Experience Platform Identity Service Co-op Graph of Private Graph gebruiken. Zie de [startpagina](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) in de gebruikershandleiding voor apparaatcoop.
   * Uit een geest van partnerschap en transparantie willen wij dat onze klanten zich bewust zijn van ons gebruik van Microsoft Azure in combinatie met Cross-Device Analytics. Adobe gebruikt Azure om grafiekgegevens van apparaten op te slaan en om overspannen-apparaat het stitching uit te voeren. Daarom worden Adobe Analytics-gegevens afwisselend doorgegeven tussen het gegevensverwerkingscentrum van Adobe en de door Adobe geleverde instanties van Microsoft Azure.
* Apparaatanalyse wordt ingeschakeld op basis van een afzonderlijke rapportsuite. Voor de rapportsuites die voor CDA zijn ingeschakeld, is het volgende vereist:
   * De rapportenreeks mag niet meer dan 500 miljoen hits per dag hebben.
   * Adobe raadt een rapportsuite aan die apparaatgegevens bevat. Dit betekent gegevens van meerdere apparaattypen (web, app, enz.). Sommige organisaties noemen dit concept een &quot;globaal&quot; rapportenpakket, hoewel CDA vanuit geografisch oogpunt niet strikt algemeen hoeft te zijn. Cross-Device Analytics werkt niet op meerdere rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Uw implementatie moet aan de volgende vereisten voldoen:
   * De nieuwste versie van de Experience Cloud ID Service moet worden geïmplementeerd. Zie de [startpagina](https://docs.adobe.com/content/help/en/id-service/using/home.html) in de gebruikershandleiding van Experience Cloud Identity Service. Bij de meeste implementaties waarbij gebruik wordt gemaakt van Adobe Experience Platform Launch is ECID al geïmplementeerd.
   * Roep de `setCustomerIDs` functie aan wanneer een individu kan worden geïdentificeerd, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [setCustomerIDs](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/setcustomerids.html) in de gebruikershandleiding Experience Cloud Identity Service.

## Beperkingen

Cross-Device Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop deze kan worden gebruikt.

* CDA is alleen beschikbaar via de analysewerkruimte.
* Het plaatsen kan niet over rapportreeksen voorkomen zoals die in de eerste vereisten hierboven worden beschreven.
* Rapportreeksen van Adobe Analytics kunnen niet aan meer dan één IMS org worden toegewezen. Aangezien CDA apparaten vastlegt binnen een bepaalde rapportsuite, kan CDA niet worden gebruikt om gegevens te koppelen aan meerdere IMS-organen.
* CDA is momenteel niet compatibel met Customer Attributes. De Attributen van de klant kunnen niet worden gebruikt om een virtueel CDA- rapportreeks, binnen dwars-apparatensegmenten, of voor rapportering binnen een het werkruimteproject van de Analyse tot stand te brengen dat op een CDA virtueel rapportreeks gebaseerd is.
   > [!TIP] Hoewel de Attributen van de Klant niet in CDA kunnen worden gebruikt, baseren beide eigenschappen zich op de `setCustomerIDs` functie. Deze twee eigenschappen kunnen in afzonderlijke (virtuele) rapportreeksen samenvallen.
* CDA vereist of de Grafiek Co-op of PrivéGrafiek. Apparaatgrafieken van derden worden niet ondersteund.
* Verouderde analyse-id&#39;s worden niet ondersteund. Alleen bezoekers met de ID&#39;s van Experience Cloud worden vastgezet.
* De klantenservice biedt nog geen volledige ondersteuning voor deze functie. Het [Cross-Device Analytics-forum](https://forums.adobe.com/community/experience-cloud/analytics-cloud/analytics/cross-device-analytics/overview) kan worden gebruikt voor ondersteuning voor deze functie, die actieve en directe betrokkenheid van Adobe Product Managers omvat.
* Analytics voor verschillende apparaten maakt gebruik van een virtuele rapportsuite en de verwerking van de rapporttijd, die hun eigen beperkingen hebben. Zie [Virtuele rapportsuites](../vrs/vrs-about.md) en de tijdverwerking [van het](../vrs/vrs-report-time-processing.md) Rapport voor meer informatie over deze beperkingen.
* De 1.4-API wordt niet ondersteund. Power BI-connectors en Report Builder vertrouwen beide op de 1.4-API en zijn daarom niet compatibel met CDA.
* Als uw organisatie de Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Nieuwe apparaten die uw site bezoeken, kunnen maximaal twee weken duren voordat ze door de Co-op grafiek worden verwerkt. De mate van stitching in CDA voor de meest recente twee weken is doorgaans lager dan voor datumbereiken die ouder zijn dan twee weken. Adobe is van plan om de Co-op-grafiek in de toekomst te verbeteren tot een dagelijks vernieuwde grafiek.
* Historische gegevens in de virtuele rapportsuite veranderen op basis van het herkennen en aansluiten van apparaten door Adobe. De gegevens in de bronrapportsuite veranderen niet.

Als uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u [Apparaatanalyse](cda-setup.md)instellen.
