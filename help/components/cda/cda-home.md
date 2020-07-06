---
title: Cross-device Analytics
description: Analytics op verschillende apparaten wijzigt uw gegevens van apparaatfocus naar persoonlijke focus door apparaatgegevens aan elkaar te hechten.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '965'
ht-degree: 1%

---


# Cross-device Analytics

Analytics op verschillende apparaten is een functie waarmee Analytics van een apparaatgecentreerde weergave wordt getransformeerd naar een persoonlijk gecentreerde weergave. Deze functie gebruikt de Co-op Grafiek van de Dienst van de Identiteit van het Adobe Experience Platform of Privé Grafiek om te identificeren welke apparaten tot individuen behoren, en hen te binden. Dit heeft tot gevolg dat analisten begrip hebben voor het gedrag van gebruikers in browsers, apparaten of apps. U kunt CDA gebruiken om vragen zoals:

* Hoeveel mensen interageren met mijn merk? Hoeveel en welke soorten apparaten gebruiken zij? Hoe overlappen ze elkaar?
* Hoe vaak beginnen mensen met een taak op een mobiel apparaat en gaan ze later over naar een desktop-pc om de taak te voltooien? Leidt het aanwijzen van campagnes die op één apparaat landen tot omschakeling elders?
* Hoe verandert mijn begrip van campagnedoeltreffendheid als ik rekening houd met apparatuurreizen? Hoe verandert mijn trechter-analyse?
* Wat zijn de gemeenschappelijkste wegen die gebruikers van één apparaat aan een ander nemen? Waar komen ze uit? Waar slagen ze?
* Hoe verschilt het gedrag van gebruikers met meerdere apparaten van de gebruikers met één apparaat?

Wanneer de apparaten worden vastgezet, veranderlijke persistentie wordt gedragen over apparaten. Een gebruiker bezoekt bijvoorbeeld eerst uw site via een advertentie op zijn desktopcomputer. Deze gebruiker zoekt uw mobiele app, installeert deze en koopt deze uiteindelijk op zijn mobiele apparaat. Met Cross-Device Analytics kunnen inkomsten worden toegeschreven aan de advertentie waarop ze op hun desktopcomputer hebben geklikt.

Zie [Reis IQ: Analytics Spark-pagina](http://adobe.ly/aacda) voor verschillende apparaten voor meer informatie over de mogelijkheden en functies van Analytics voor verschillende apparaten.

## Vereisten

Voor Analytics op verschillende apparaten is het volgende vereist. Werk met teams binnen uw organisatie en uw accountmanager van Adobe om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat Analytics voor verschillende apparaten niet kan worden ingeschakeld of dat de gegevens niet correct worden opgeslagen.

* De gegevens van uw organisatie moeten zich in het datacenter van het Pacific Northwest van Adobe bevinden. Er is voorzien in steun voor datacentra in andere regio&#39;s van de wereld.
* Neem contact op met de accountmanager van uw organisatie om de volgende belangrijke punten vast te stellen:
   * Er moet een contract worden ondertekend met Adobe Analytics Ultimate.
   * Uw organisatie moet de Coop Grafiek van de Dienst van de Identiteit van het Adobe Experience Platform of PrivéGrafiek gebruiken. Zie de [startpagina](https://docs.adobe.com/content/help/en/device-co-op/using/home.html) in de gebruikershandleiding voor apparaatcoop.
   * Uit een geest van partnerschap en transparantie willen wij dat onze klanten zich bewust zijn van ons gebruik van Microsoft Azure in combinatie met Cross-Device Analytics. Adobe gebruikt Azure om grafiekgegevens van apparaten op te slaan en om overspannen-apparaat het stitching uit te voeren. Daarom worden Adobe Analytics-gegevens afwisselend doorgegeven tussen het gegevensverwerkingscentrum van Adobe en de door Adobe geleverde instanties van Microsoft Azure.
* Analytics voor verschillende apparaten wordt ingeschakeld op basis van een aantal afzonderlijke rapporten. Voor de rapportsuites die voor CDA zijn ingeschakeld, is het volgende vereist:
   * De rapportenreeks mag niet meer dan 500 miljoen hits per dag hebben.
   * Adobe raadt een rapportsuite aan die apparaatgegevens bevat. Dit betekent gegevens van meerdere apparaattypen (web, app, enz.). Sommige organisaties noemen dit concept een &quot;globaal&quot; rapportenpakket, hoewel CDA vanuit geografisch oogpunt niet strikt algemeen hoeft te zijn. Analytics voor meerdere apparaten werkt niet in verschillende rapportsuites en combineert ook geen gegevens van meerdere rapportsuites.
* Uw implementatie moet aan de volgende vereisten voldoen:
   * De nieuwste versie van de Experience Cloud ID Service moet worden geïmplementeerd. Zie de [startpagina](https://docs.adobe.com/content/help/nl-NL/id-service/using/home.html) in de gebruikershandleiding van de Experience Cloud Identity Service. De meeste implementaties die gebruikmaken van het Adobe Experience Platform Launch hebben waarschijnlijk al ECID geïmplementeerd.
   * Roep de `setCustomerIDs` functie aan wanneer een individu kan worden geïdentificeerd, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Zie [setCustomerIDs](https://docs.adobe.com/content/help/en/id-service/using/id-service-api/methods/setcustomerids.html) in de Experience Cloud Identity Service gebruikershandleiding.

## Beperkingen

Analytics is een baanbrekende en robuuste functie, maar heeft beperkingen in de manier waarop het kan worden gebruikt.

* CDA is alleen beschikbaar via Analysis Workspace.
* Het plaatsen kan niet over rapportreeksen voorkomen zoals die in de eerste vereisten hierboven worden beschreven.
* Adobe Analytics-rapportsuites kunnen niet aan meer dan één IMS org worden toegewezen. Aangezien CDA apparaten vastlegt binnen een bepaalde rapportsuite, kan CDA niet worden gebruikt om gegevens te koppelen aan meerdere IMS-organen.
* CDA is momenteel niet compatibel met Customer Attributes. De Attributen van de klant kunnen niet worden gebruikt om een virtueel CDA- rapportreeks, binnen dwars-apparatensegmenten, of voor rapportering binnen een het werkruimteproject van de Analyse tot stand te brengen dat op een CDA virtueel rapportreeks gebaseerd is.
   > [!TIP] Hoewel de Attributen van de Klant niet in CDA kunnen worden gebruikt, baseren beide eigenschappen zich op de `setCustomerIDs` functie. Deze twee eigenschappen kunnen in afzonderlijke virtuele rapportreeksen samenvallen.
* CDA vereist of de Grafiek Co-op of PrivéGrafiek. Apparaatgrafieken van derden worden niet ondersteund.
* Verouderde Analytics-id&#39;s worden niet ondersteund. Alleen bezoekers met Experience Cloud-id&#39;s zijn gebonden.
* Analytics voor verschillende apparaten gebruikt een virtuele rapportsuite en meldt tijdverwerking, die hun eigen beperkingen hebben. Zie [Virtuele rapportsuites](../vrs/vrs-about.md) en de tijdverwerking [van het](../vrs/vrs-report-time-processing.md) Rapport voor meer informatie over deze beperkingen.
* De 1.4-API wordt niet ondersteund. Power BI-connectors en Report Builder vertrouwen beide op de 1.4-API en zijn daarom niet compatibel met CDA.
* Als uw organisatie de Privé Grafiek gebruikt, nemen de nieuwe apparaten tot 24 uren om worden vastgemaakt.
* Nieuwe apparaten die uw site bezoeken, kunnen maximaal twee weken duren voordat ze door de Co-op grafiek worden verwerkt. De mate van stitching in CDA voor de meest recente twee weken is doorgaans lager dan voor datumbereiken die ouder zijn dan twee weken.
* Historische gegevens in de virtuele rapportsuite veranderen op basis van het herkennen en aansluiten van apparaten door Adobe. De gegevens in de bronrapportsuite veranderen niet.

Als aan alle vereisten van uw organisatie is voldaan en u begrijpt welke beperkingen er gelden, kunt u Analytics [voor verschillende apparaten](cda-setup.md)instellen.
