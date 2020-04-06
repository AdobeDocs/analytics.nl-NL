---
description: 'De id''s die u verzendt, hebben niet altijd betrekking op alle raakgegevens die door Analytics aan de betrokkene kunnen worden gekoppeld. Analytics kan een uitgebreide reeks id''s maken om deze bijbehorende gegevens op te nemen in de aanvragen voor gegevensprivacy. U kunt deze optie aanvragen met een optionele parameter voor elk verzoek om gegevensprivacy dat u indient, toegevoegd aan de JSON-aanvraag '
title: ID-uitbreiding
uuid: 2672d17d-c957-4e08-8dd9-16d54bf2be18
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# ID-uitbreiding

De id&#39;s die u verzendt, hebben niet altijd betrekking op alle raakgegevens die door Analytics aan de betrokkene kunnen worden gekoppeld. Analytics kan een uitgebreide reeks id&#39;s maken om deze bijbehorende gegevens op te nemen in de aanvragen voor gegevensprivacy. U kunt deze optie aanvragen met een optionele parameter voor elk gegevensprivacyverzoek dat u verzendt, toegevoegd aan de JSON-aanvraag:

```
"expandIds": true
```

Zie het [Voorbeeld JSON Verzoek](/help/admin/c-data-governance/gdpr-submit-access-delete.md#sample-json-request) voor een voorbeeld van hoe te om deze optie met het verzoek te omvatten. Raadpleeg de API-documentatie [van de](https://www.adobe.io/apis/experienceplatform/gdpr.html)Privacy Service voor meer informatie.

<table id="table_A10CA8DC8C1643CF84A4DF30A6740D51"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Overwegingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Expansie Cookie-id </p> </td> 
   <td colname="col2"> <p>Veel klanten van Analytics gebruikten oorspronkelijk de (Verouderde) <a href="https://marketing.adobe.com/resources/help/en_US/whitepapers/cookies/cookies_analytics.html"> Analytics Cookie </a>, maar gebruiken nu de <a href="https://marketing.adobe.com/resources/help/en_US/mcvid/"> Identiteitsdienst (ECID) </a>, die vroeger als de Dienst van identiteitskaart van de Marketing Cloud (MCID) wordt bekend. Voor hun websitebezoekers die voor het eerst na de overgang zijn bezocht, bestaat alleen de ECID. Voor degenen die voor het eerst een bezoek hebben gebracht toen alleen de Oudere Koek beschikbaar was, maar die sindsdien een bezoek hebben gebracht: Sommige gegevens hebben beide cookies, maar de oudere gegevens hebben alleen de Analytics Cookie en in zeldzame gevallen hebben de nieuwste gegevens alleen een ECID. </p> <p>U wilt ervoor zorgen dat alle gegevens voor een bezoeker worden gevonden die via een Analytics-cookie (Visitor ID) of ECID zijn geïdentificeerd. Daarom als u momenteel ECID gebruikt en eerder Analytics Cookie gebruikte, wanneer u een verzoek indient gebruikend één van beide type van identiteitskaart, zou u beide IDs in het verzoek moeten omvatten, of de expandIds optie specificeren. Wanneer u expandIds opgeeft, controleert Adobe op andere ECID's of Analytics Cookies die overeenkomen met cookies die u opgeeft. De aanvraag wordt automatisch uitgebreid met deze zojuist geïdentificeerde cookie-id's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste id voor uitbreiding van cookie-id </p> </td> 
   <td colname="col2"> <p>Op e-commercewebsites is het niet ongebruikelijk dat een bezoeker door de site bladert, dingen aan zijn winkelwagentje toevoegt en vervolgens het afrekenproces start voordat hij of zij zich bij de site aanmeldt. Als ID wordt gebruikt om gebruikers voor een verzoek van de Privacy van Gegevens te identificeren slechts in een douanevariabele wordt opgeslagen wanneer de gebruiker het programma wordt geopend, dan zal deze pre-login activiteit niet met identiteitskaart worden geassocieerd. Met behulp van de Analytics-cookie-id kunnen klanten het bladeren dat is uitgevoerd voordat ze zich aanmelden, koppelen aan de aanschaf na aanmelding, aangezien de cookie-id tijdens de aanmelding aanwezig blijft. </p> <p>Stel dat in uw implementatie een aanmeldings-id (CRM-id, gebruikersnaam, loyaliteitsnummer, e-mailadres, enzovoort, of een hash van een van deze waarden) wordt opgeslagen in een aangepaste variabele (prop of eVar) of een aangepaste bezoeker-id. Vervolgens wordt deze id gebruikt voor een verzoek om toegang tot Data Privacy. Het kan de betrokkene verbazen dat informatie over al hun browsers niet wordt geretourneerd als onderdeel van een toegangsaanvraag, vooral als je objecten die je hebt bekeken maar nog niet hebt gekocht, tot hen hebt bevorderd. </p> <p>De verwerking van de Privacy van Gegevens van Analytics steunt daarom de Uitbreiding van identiteitskaart, waar de Analytics alle koekjesidentiteitskaart's vindt die in de zelfde klap zoals om het even welke douane ID voorkomen en dan het verzoek uitbreidt om die IDs eveneens te omvatten. </p> <p>Wanneer expandIDs samen met om het even welke namespace buiten een koekjesnamespace wordt gespecificeerd, zal het verzoek worden uitgebreid om het even welke koekjesidentiteitskaart (ECID of Cookie van Analytics) te omvatten, die in klappen wordt gevonden die om het even welke gespecificeerde IDs bevatten. De uitbreiding van de cookie-id, zoals hierboven beschreven, wordt vervolgens uitgevoerd op alle nieuw gevonden cookie-id's. </p> <p>Wanneer de optie expandIDs wordt gebruikt voor een toegangsverzoek en de gespecificeerde identiteitskaart een etiket van ID-PERSON heeft, dan zullen twee reeksen dossiers worden teruggekeerd. De eerste set (de personenset) bevat alleen gegevens uit treffers waar de opgegeven id is gevonden. De tweede set (de apparaatset) bevat alleen gegevens uit treffers van de uitgebreide id's, waarbij de opgegeven id niet aanwezig was. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tijdens de eerste maanden nadat de Privacy van Gegevens live ging, vroeg het overgrote deel van de verzoeken van de Privacy van Gegevens van Analytics geen uitbreiding van identiteitskaart, maar het bepalen van de aangewezen waarde voor uw organisatie is aan u. Vraag uw juridische team of id-uitbreiding vereist is voor uw gegevens aan de hand van de id&#39;s die u gebruikt en de gegevens die u verzamelt in Adobe Analytics. Een primaire overweging moet zijn dat op een gedeeld apparaat, waarvan meerdere gebruikers uw site hebben bezocht, het gebruik van ID-uitbreiding gegevens van hits van andere gebruikers van het apparaat bevat in gegevens die worden geretourneerd door toegangsaanvragen (in het apparaatbestand). Zelfs als u de beste praktijken in etikettering hebt gevolgd, zodat geen privé gegevens in het apparatendossier, zoals bezochte pagina&#39;s worden omvat, zal het apparatendossier het aantal bezochte pagina&#39;s en de tijden van elk van die bezoeken bevatten. Is het OK als u deze informatie deelt met iemand die misschien niet de bezoeker is geweest?

Als u voor een verwijderingsaanvraag een niet-cookie-id gebruikt (een andere id dan de CID of het Analytics-cookie) om treffers te identificeren die moeten worden verwijderd en die ID een ID-DEVICE-label heeft, wordt het aantal unieke bezoekers in rapporten gewijzigd, omdat slechts enkele exemplaren van de cookie-id&#39;s anoniem blijven, terwijl andere ongewijzigd blijven. Als u geen id-uitbreiding opgeeft, wordt u aangeraden een cookie-id voor aanvragen te gebruiken of id&#39;s met een ID-PERSON-label te gebruiken.

Wanneer Adobe id uitbreidt, kan een extra volledige gegevensscan nodig zijn. Hierdoor duurt het langer voordat Adobe de aanvraag heeft voltooid en wordt vaak een week aan de verwerkingstijd toegevoegd.

## Andere vlaggen voor privacyaanvraag

Naast de markering &quot;expandIDs&quot; ondersteunt Analytics twee andere markeringen die kunnen worden doorgegeven als onderdeel van een verzoek om gegevensprivacy. Deze markeringen met hun standaardwaarden zijn:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In de toekomst ondersteunt de &quot;analyticsDeleteMethod&quot; mogelijk een waarde van &quot;purge&quot; naast de standaardwaarde van &quot;anonymize&quot;. Als deze functie wordt ondersteund, wordt de hele hit verwijderd en worden de waarden van aanraakvelden met DEL-labels niet bijgewerkt.

Naast zijn standaardwaarde, steunt het prioritaire gebied ook een waarde van &quot;laag&quot;. U moet deze waarde opgeven voor verzoeken die niet het resultaat zijn van een verzoek van de betrokkene en dus niet de wettelijke verplichting hebben om binnen 30 dagen te worden ingevuld. Adobe raadt het gebruik van de API voor de privacyservice af om andere redenen dan het indienen van aanvragen door de betrokkene. De API van de Privacy Service is geen geschikt instrument voor het opschonen of repareren van gegevens en zal onbedoelde gevolgen hebben.

>[!NOTE] De API [van de](https://www.adobe.io/apis/experienceplatform/gdpr.html) Privacy Service is verstrekt om u te helpen verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan van invloed zijn op het vermogen van Adobe om snel door de gebruiker geïnitieerde verzoeken om gegevensprivacy met hoge prioriteit aan te bieden voor andere Adobe-klanten. We vragen u de API voor privacyservice niet te gebruiken voor andere doeleinden, zoals het wissen van gegevens die per ongeluk zijn verzonden door grote groepen bezoekers.

U moet er ook op letten dat bezoekers die een hit hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een aanvraag voor het verwijderen van gegevensprivacy, hun statusgegevens opnieuw kunnen instellen. De volgende keer dat de bezoeker terugkeert naar uw website, wordt hij of zij een nieuwe bezoeker. Alle eVar-toewijzing wordt opnieuw gestart, evenals informatie zoals bezoeknummers, referenties, bezochte eerste pagina, enz. Deze bijwerking is ongewenst in situaties waarin u gegevensvelden wilt wissen en benadrukt één reden waarom de API voor de privacyservice niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen te werken met ons consultatieteam van de Engineering Architect voor verdere controle en om de moeite te nemen om eventuele problemen met PII&#39;s of gegevens te verwijderen.

