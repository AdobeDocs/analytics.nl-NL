---
description: De id's die u verzendt, hebben niet altijd betrekking op alle raakgegevens die door Analytics aan het onderwerp Gegevens kunnen worden gekoppeld. Analytics kan een uitgebreide reeks id's maken om deze gekoppelde data op te nemen in de Data Privacy-aanvragen. U kunt deze optie aanvragen met een optionele parameter voor elke Data Privacy-aanvraag die u verzendt, toegevoegd aan de JSON-aanvraag
title: Id-uitbreiding
feature: Data Governance
exl-id: 312a249f-e0e7-44da-bb3d-b19f1bb4c706
source-git-commit: 1ca7040156f7f2105a9625f921de3d90b4175056
workflow-type: tm+mt
source-wordcount: '1351'
ht-degree: 32%

---

# Id-uitbreiding

De id&#39;s die u verzendt, hebben niet altijd betrekking op alle raakgegevens die door Analytics aan het onderwerp Gegevens kunnen worden gekoppeld. Analytics kan een uitgebreide reeks id&#39;s maken om deze gekoppelde data op te nemen in de Data Privacy-aanvragen. U kunt deze optie aanvragen met een optionele parameter voor elke Data Privacy-aanvraag die u verzendt, toegevoegd aan de JSON-aanvraag:

```
"expandIds": true
```

Raadpleeg de [Privacy Service-API-documentatie](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html) voor meer details.


| Type | Overwegingen |
| --- | --- |
| Cookie-id-expansie | Veel klanten van Analytics gebruikten oorspronkelijk de (Verouderd) [Analytische cookie](https://experienceleague.adobe.com/docs/core-services/interface/administration/ec-cookies/cookies-privacy.html?lang=en), maar nu de [Experience Cloud Identity Service (ECID)](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en). Voor hun websitebezoekers die voor het eerst na de overgang op de website komen, bestaat alleen de ECID. Voor degenen die voor het eerst een bezoek hebben gebracht toen alleen de Oudere Koek beschikbaar was, maar die sindsdien een bezoek hebben gebracht: sommige van hun gegevens hebben beide cookies . De oudere gegevens hebben echter alleen de Analytics Cookie en in zeldzame gevallen hebben de nieuwste gegevens alleen een ECID.<p>Zorg ervoor dat u alle gegevens vindt voor een bezoeker die via een Analytics-cookie (Visitor ID) of ECID is geïdentificeerd. Als u momenteel de ECID gebruikt en eerder de Analytics Cookie hebt gebruikt, moet u beide id&#39;s in de aanvraag opnemen als u een aanvraag indient met een van beide typen ID, of de `expandIds` optie. Wanneer u `expandIds`, controleert Adobe op andere ECID&#39;s of Analytics Cookies die overeenkomen met cookies die u opgeeft. Het verzoek wordt automatisch uitgebreid om deze zojuist geïdentificeerde cookie-id&#39;s op te nemen. |
| Aangepaste id voor cookie-id-expansie | Op e-commercewebsites is het niet ongebruikelijk dat een bezoeker door de site bladert, dingen aan de winkelwagen toevoegt en vervolgens het afrekenproces start voordat hij of zij zich bij de site heeft aangemeld. Als ID wordt gebruikt om gebruikers voor een verzoek van de Privacy van Gegevens te identificeren slechts in een douanevariabele wordt opgeslagen wanneer de gebruiker het programma wordt geopend, dan wordt deze pre-login activiteit niet geassocieerd met identiteitskaart Met behulp van de Analytics-cookie-id kunnen klanten ervoor kiezen om het bladeren van vóór de aanmelding koppelen aan de aankoop na de aanmelding, aangezien de cookie-id tijdens de aanmelding aanwezig blijft.<p>Stel dat in uw implementatie een aanmeldings-id (CRM-id, gebruikersnaam, loyaliteitsnummer, e-mailadres, enzovoort, of een hash van een van deze waarden) wordt opgeslagen in een aangepaste variabele (prop of eVar) of een aangepaste bezoekers-id. Vervolgens wordt deze id gebruikt voor een aanvraag voor toegang tot Data Privacy. Het onderwerp Gegevens kan verrast zijn dat informatie over al hun het doorbladeren niet als deel van een toegangsverzoek wordt teruggegeven, vooral als u punten hebt bevorderd die werden bekeken maar nog niet gekocht. Daarom ondersteunt Analytics Data Privacy-verwerking Id-uitbreiding, waardoor Analytics alle cookie-id&#39;s vindt die voorkomen in dezelfde treffer als alle aangepaste id&#39;s en vervolgens de aanvraag uitbreidt zodat deze id&#39;s daarin ook worden opgenomen.<p>Wanneer `expandIDs` samen met een andere naamruimte dan een cookie-naamruimte wordt de aanvraag uitgebreid met alle cookie-id&#39;s (ECID of Analytics Cookie) die worden gevonden in hits met een van de opgegeven id&#39;s. De uitbreiding van de cookie-id, zoals hierboven beschreven, wordt vervolgens uitgevoerd op alle nieuw gevonden cookie-id&#39;s.<p>Wanneer de `expandIDs` wordt gebruikt voor een toegangsverzoek en de gespecificeerde identiteitskaart heeft een etiket van ID-PERSON, dan zullen twee reeksen dossiers worden teruggekeerd. De eerste reeks (de personenreeks) bevat alleen data uit treffers waar de opgegeven id is gevonden. De tweede reeks (de apparaatreeks) bevat alleen data uit treffers van de uitgebreide id&#39;s waarbij de opgegeven id niet aanwezig was. |

{style=&quot;table-layout:auto&quot;}

## Wanneer moet u id-uitbreiding gebruiken?

Tijdens de eerste maanden nadat Data Privacy live ging, verzocht het overgrote deel van de verzoeken van de Privacy van de Gegevens van Analytics niet om uitbreiding van identiteitskaart. Het is echter aan u om de juiste waarde voor uw organisatie te bepalen. Vraag uw juridische team of id-uitbreiding vereist is voor uw gegevens aan de hand van de id&#39;s die u gebruikt en de gegevens die u verzamelt in Adobe Analytics.

Een primaire overweging zou kunnen zijn: Op een gedeeld apparaat, waarvan meerdere gebruikers uw site hebben bezocht, bevat het gebruik van ID-uitbreiding gegevens van hits van andere gebruikers van het apparaat in gegevens die worden geretourneerd door toegangsaanvragen (in het apparaatbestand). Zelfs als u de beste praktijken in etikettering hebt gevolgd (bijvoorbeeld, wordt geen privé gegevens opgenomen in het apparatendossier, zoals bezochte pagina&#39;s) bevat het apparatendossier het aantal bezochte pagina&#39;s en de tijden van elk van die bezoeken. U kunt zich afvragen: Is het oké als je deze informatie deelt met iemand die misschien niet de bezoeker is geweest?

Wanneer ID-uitbreiding *niet* gebruikt voor een verwijderingsaanvraag: als u een niet-cookie-id gebruikt (een andere id dan de cookie ECID of Analytics) om hits te identificeren die moeten worden verwijderd en die ID een ID-DEVICE-label heeft, wordt het aantal unieke bezoekers in rapporten gewijzigd. Dit komt doordat slechts enkele exemplaren van de cookie-id&#39;s worden geanonimiseerd, terwijl andere ongewijzigd blijven. Als u geen uitbreiding van identiteitskaart specificeert, dan adviseren wij dat u of een koekjesidentiteitskaart voor verzoeken gebruikt, of identiteitskaart met een identiteitskaart-PERSON etiket gebruikt.

Als Adobe ID uitbreidt, is mogelijk een extra volledige gegevensscan nodig. Dit verhoogt de tijd dat het Adobe vergt om het verzoek te voltooien, vaak toevoegend een week aan de verwerkingstijd.

## Andere markeringen voor Data Privacy-aanvragen

Naast de markering “expandIDs” ondersteunt Analytics twee andere markeringen die kunnen worden doorgegeven als onderdeel van een Data Privacy-aanvraag. Deze markeringen met hun standaardwaarden zijn:

```
"analyticsDeleteMethod": "anonymize"
"priority": "normal"
```

In de toekomst `analyticsDeleteMethod` kan een waarde van &quot;purge&quot; ondersteunen, naast de standaardwaarde van &quot;anonymize&quot;. Als deze functie wordt ondersteund, wordt de volledige hit verwijderd en worden de waarden van aanraakvelden met DEL-labels niet bijgewerkt.

Naast de standaardwaarde worden `priority` in het veld wordt ook de waarde &quot;low&quot; ondersteund. U moet deze waarde opgeven voor verzoeken die niet het resultaat zijn van een verzoek betreffende een betrokkene en dus niet de wettelijke verplichting hebben om binnen een bepaalde termijn te worden voltooid.

## Gebruik van de Privacy Service-API

>[!IMPORTANT]
>
>Adobe staat het gebruik van de [Privacy Service-API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html) om andere redenen dan geldige verzoeken die door de betrokkene zijn ingediend. De Privacy Service-API is geen geschikt hulpmiddel voor het opschonen of repareren van gegevens. Elk misbruik van de Privacy Service-API voor verzoeken die niet onder de gegevensbank vallen, zal onbedoelde gevolgen hebben. De Privacy Service API wordt verstrekt aan Adobe klanten om u te helpen de verzoeken van de Privacy van Gegevens vervullen, die tijdgevoelig zijn. Het gebruik van deze API voor andere doeleinden wordt niet ondersteund door Adobe en kan een nadelige invloed hebben op de snelheid waarmee Adobe door de gebruiker geïnitieerde Data Privacy-aanvragen met hoge prioriteit voor andere Adobe-klanten kan afhandelen. We vragen u de Privacy Service-API niet te gebruiken voor andere doeleinden, zoals gegevenshygiëne of het wissen van gegevens die per ongeluk zijn verzonden door grote groepen bezoekers.

Bedenk ook dat voor bezoekers die een treffer hebben verwijderd (bijgewerkt of geanonimiseerd) als gevolg van een Data Privacy-verwijderingsaanvraag, de statusgegevens worden hersteld. De volgende keer dat de bezoeker uw website bezoekt, wordt deze een nieuwe bezoeker. Alle eVar-attributie wordt opnieuw gestart, evenals informatie als aantal bezoeken, referrers, bezochte eerste pagina, enz. Het resultaat is ongewenst in situaties waarin u gegevensvelden wilt wissen en geeft één reden aan waarom de Privacy Service-API niet geschikt is voor dit gebruik.

Neem contact op met uw accountmanager (CSM) om samen te werken met ons consultatieteam van de Engineering Architect om verdere revisie uit te voeren en de moeite te leveren om eventuele PII&#39;s te verwijderen of gegevensproblemen op te lossen.
