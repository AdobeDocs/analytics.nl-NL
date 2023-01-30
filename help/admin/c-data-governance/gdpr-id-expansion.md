---
description: De id's die u verzendt, hebben niet altijd betrekking op alle treffers die door Analytics aan de geregistreerde persoon kunnen worden gekoppeld. Analytics kan een uitgebreide reeks id's maken om deze gekoppelde data op te nemen in de Data Privacy-aanvragen. U kunt deze optie aanvragen met een optionele parameter voor elke Data Privacy-aanvraag die u verzendt, toegevoegd aan de JSON-aanvraag
title: Id-uitbreiding
feature: Data Governance
exl-id: 312a249f-e0e7-44da-bb3d-b19f1bb4c706
source-git-commit: 4bbed2efde0574bc9f5f6a78a022a22490e75549
workflow-type: tm+mt
source-wordcount: '1338'
ht-degree: 96%

---

# Id-uitbreiding

De id&#39;s die u verzendt, hebben niet altijd betrekking op alle treffers die door Analytics aan de geregistreerde persoon kunnen worden gekoppeld. Analytics kan een uitgebreide reeks id&#39;s maken om deze gekoppelde data op te nemen in de Data Privacy-aanvragen. U kunt deze optie aanvragen met een optionele parameter voor elke Data Privacy-aanvraag die u verzendt, toegevoegd aan de JSON-aanvraag:

```
"expandIds": true
```

Raadpleeg de [Privacy Service-API-documentatie](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html) voor meer details.

<table id="table_A10CA8DC8C1643CF84A4DF30A6740D51"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Type </th> 
   <th colname="col2" class="entry"> Overwegingen </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Cookie-id-expansie </p> </td> 
   <td colname="col2"> <p>Veel Analytics-klanten gebruikten oorspronkelijk het (verouderde) <a href="https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-privacy.html">Analytics Cookie</a>, maar gebruiken nu de <a href="https://experienceleague.adobe.com/docs/id-service/using/home.html">Identity Service (ECID)</a>, die vroeger Marketing Cloud ID Service (MCID) werd genoemd. Voor hun websitebezoekers die voor het eerst na de overgang op de website komen, bestaat alleen de ECID. Voor degenen die voor het eerst de site hebben bezocht toen alleen het verouderde cookie beschikbaar was, maar die de site sindsdien opnieuw hebben bezocht: sommige data hebben beide cookies, maar de oudere data hebben alleen het Analytics-cookie, en in zeldzame gevallen hebben de nieuwste data alleen een ECID. </p> <p>U wilt ervoor zorgen dat u alle gegevens vindt voor een bezoeker die via een Analytics-cookie (Visitor ID) of ECID is geïdentificeerd. Daarom moet u, als u momenteel de ECID gebruikt en vroeger het Analytics-cookie gebruikte, steeds wanneer u een aanvraag verzendt met één van beide id-typen, beide id's in de aanvraag opnemen, of de optie voor expandIds specificeren. Wanneer u de optie voor expandIds specificeert, controleert Adobe op andere ECID's of Analytics-cookies die overeenkomen met cookie-id's die u opgeeft. De aanvraag wordt automatisch uitgebreid met deze zojuist geïdentificeerde cookie-id's. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Aangepaste id voor cookie-id-expansie </p> </td> 
   <td colname="col2"> <p>Op e-commercewebsites is het niet ongebruikelijk dat een bezoeker door de site bladert, dingen aan de winkelwagen toevoegt en vervolgens het afrekenproces start voordat hij of zij zich bij de site heeft aangemeld. Als de gebruikte id voor de identificatie van gebruikers voor een Data Privacy-aanvraag alleen wordt opgeslagen in een aangepaste variabele wanneer de gebruiker is aangemeld, wordt deze pre-aanmeldingsactiviteit niet aan de id gekoppeld. Met behulp van de Analytics-cookie-id kunnen klanten ervoor kiezen om het bladeren van vóór de aanmelding koppelen aan de aankoop na de aanmelding, aangezien de cookie-id tijdens de aanmelding aanwezig blijft. </p> <p>Stel dat in uw implementatie een aanmeldings-id (CRM-id, gebruikersnaam, loyaliteitsnummer, e-mailadres, enzovoort, of een hash van een van deze waarden) wordt opgeslagen in een aangepaste variabele (prop of eVar) of een aangepaste bezoekers-id. Vervolgens wordt deze id gebruikt voor een aanvraag voor toegang tot Data Privacy. Misschien is de geregistreerde persoon verbaasd dat niet alle informatie over het bladeren wordt geretourneerd als deel van een toegangsaanvraag, vooral als u objecten hebt aanbevolen die zijn bekeken, maar nog niet gekocht. </p> <p>Daarom ondersteunt Analytics Data Privacy-verwerking Id-uitbreiding, waardoor Analytics alle cookie-id's vindt die voorkomen in dezelfde treffer als alle aangepaste id's en vervolgens de aanvraag uitbreidt zodat deze id's daarin ook worden opgenomen. </p> <p>Wanneer expandIDs wordt gespecificeerd met andere naamruimten behalve een cookienaamruimte, wordt de aanvraag uitgebreid naar alle cookie-id's (ECID of Analytics-cookie) die worden gevonden in treffers met een van de gespecificeerde id's. De uitbreiding van de cookie-id, zoals hierboven beschreven, wordt vervolgens uitgevoerd op alle nieuw gevonden cookie-id's. </p> <p>Wanneer de optie voor expandIDs wordt gebruikt voor een toegangsaanvraag en de gespecificeerde id een ID-PERSON-label heeft, worden twee reeksen bestanden geretourneerd. De eerste reeks (de personenreeks) bevat alleen data uit treffers waar de opgegeven id is gevonden. De tweede reeks (de apparaatreeks) bevat alleen data uit treffers van de uitgebreide id's waarbij de opgegeven id niet aanwezig was. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tijdens de eerste maanden nadat Data Privacy live was gegaan, werd in verreweg de meeste aanvragen van Analytics Data Privacy niet gevraagd om id-uitbreiding, maar het is aan u om de juiste waarde voor uw organisatie te bepalen. Overleg met uw juridische team of id-uitbreiding vereist is voor uw data aan de hand van de id&#39;s die u gebruikt en de data die u verzamelt in Adobe Analytics. Een primaire overweging moet zijn dat op een gedeeld apparaat vanwaar meerdere gebruikers uw site hebben bezocht, door het gebruik van id-uitbreiding ook data van treffers van andere gebruikers van het apparaat worden geretourneerd bij toegangsaanvragen (in het apparaatbestand). Zelfs als u de best practices voor labeling hebt gevolgd, zodat het apparaatbestand geen privédata bevat, zal het apparaatbestand wel het aantal bezochte pagina&#39;s en de tijdstippen van al deze bezoeken bevatten. Is het in orde om deze informatie te delen met iemand die misschien niet de bezoeker is geweest?

Als u voor een verwijderingsaanvraag waarbij geen id-uitbreiding wordt gebruikt, een niet-cookie-id gebruikt (een andere id dan het ECID- of Analytics-cookie) om treffers te identificeren die moeten worden verwijderd, en als deze id een ID-DEVICE-label heeft, wordt het aantal unieke bezoekers in rapporten gewijzigd, omdat slechts enkele exemplaren van de cookie-id&#39;s worden geanonimiseerd terwijl andere ongewijzigd blijven. Als u geen id-uitbreiding opgeeft, wordt u aangeraden om voor aanvragen een cookie-id te gebruiken, of id&#39;s met een ID-PERSON-label.

Wanneer Adobe id-uitbreiding uitvoert, kan een aanvullende, volledige datascan nodig zijn. Hierdoor duurt het langer voordat Adobe de aanvraag heeft voltooid en wordt vaak een week aan de verwerkingstijd toegevoegd.

## Andere markeringen voor Data Privacy-aanvragen

Naast de markering “expandIDs” ondersteunt Analytics twee andere markeringen die kunnen worden doorgegeven als onderdeel van een Data Privacy-aanvraag. Deze markeringen met hun standaardwaarden zijn:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In de toekomst ondersteunt de “analyticsDeleteMethod” mogelijk een waarde van “purge” naast de standaardwaarde van “anonymize”. Als deze functie wordt ondersteund, wordt de hele treffer verwijderd in plaats van alleen de waarden van treffervelden met DEL-labels bij te werken.

Naast de standaardwaarde ondersteunt steunt het prioriteitsveld ook een waarde van “laag”. U moet deze waarde opgeven voor aanvragen die niet het resultaat zijn van een aanvraag van een geregistreerde persoon, en waarvoor dus geen wettelijke verplichting geldt om binnen 30 dagen te zijn afgehandeld. Adobe raadt het gebruik van de Privacy Service-API af om andere redenen dan aanvragen die door geregistreerde personen zijn geïnitieerd. De Privacy Service-API is geen geschikte tool voor het opschonen of repareren van data en zal onbedoelde gevolgen hebben.

>[!NOTE]
>
>De [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html) is bedoeld om u te helpen bij het afhandelen van Data Privacy-aanvragen, die tijdsgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen. We vragen u de Privacy Service-API niet te gebruiken voor andere doeleinden, zoals het wissen van data die per ongeluk zijn verzonden tussen grote groepen bezoekers.

Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Dit bijeffect is ongewenst in situaties waarin u datavelden wilt wissen, en legt de nadruk op één reden waarom de Privacy Service-API niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen met het consultingteam van onze engineering-architect verder te controleren en zich in te spannen voor het verwijderen van eventuele PII- of dataproblemen.
