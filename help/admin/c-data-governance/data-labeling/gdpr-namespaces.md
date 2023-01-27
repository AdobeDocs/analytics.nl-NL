---
description: Elke id die u wilt kunnen zoeken, krijgt een naamruimte toegewezen, een aangepaste tekenreeks die deze id identificeert in elke variabele waarin deze wordt gebruikt in al uw rapportsuites.
title: Naamruimten
feature: Data Governance
exl-id: 421572c2-2789-48bc-b530-d48216799724
source-git-commit: 9e8607691e6b144dd9e7b7a407bb2f02d27fbb1a
workflow-type: tm+mt
source-wordcount: '890'
ht-degree: 97%

---

# Naamruimten

Elke id die u wilt kunnen zoeken, krijgt een naamruimte toegewezen, een aangepaste tekenreeks die deze id identificeert in elke variabele waarin deze wordt gebruikt in al uw rapportsuites.

De naamruimtetekenreeks wordt gebruikt om velden te identificeren die u wilt doorzoeken wanneer u een id opgeeft als onderdeel van een Data Privacy-aanvraag. Wanneer een Data Privacy-aanvraag wordt verzonden, bevat de aanvraag een JSON-sectie waarin de id&#39;s van de geregistreerde persoon zijn opgegeven die voor de aanvraag moeten worden gebruikt. Er kunnen meerdere id&#39;s worden opgenomen als onderdeel van één aanvraag voor een geregistreerde persoon. De JSON bevat het volgende:

* Een naamruimteveld met de naamruimtetekenreeks.
* Een typeveld dat voor de meeste Adobe Analytics-aanvragen de waarde “analytics” bevat.
* Een “value”-veld met de id waarnaar Analytics moet zoeken in de gekoppelde naamruimtevariabelen van al uw rapportsuites.

Raadpleeg de [Experience Cloud Data Privacy API-documentatie](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html) voor meer informatie.

## Cookie-id

Verouderd Analytics-trackingcookie, ook wel Adobe Analytics-id (AAID) genoemd:

```
{
   namespace: "AAID",
   type: "standard",
   value: "2CCEEAE88503384F-1188000089CA"
}
```

De waarde moet worden opgegeven als twee hexadecimale getallen, gescheiden door een streepje. Alle hexadecimale cijfers die alfabetische tekens zijn, moeten worden opgegeven in hoofdletters. De hexadecimale waarden mogen geen voorloopnullen hebben (houd rekening met het verschil met dezelfde waarde in de afgeschafte vorm, waarbij voorloopnullen zijn vereist).

Het is ook acceptabel om `"namespaceId": 10` te gebruiken in plaats van of in aanvulling op `"namespace": "AAID"`, en het kan zijn dat sommige andere Adobe-producten dit formulier gebruiken.

## Cookie voor het bijhouden van oude analyses: Vervangen formulier

```
{
   "namespace": "visitorId",
   "type": "analytics",
   "value": "2cceeae88503384f-00001188000089ca"
}
```

Afgeschaft formulier:

De waarde moet worden opgegeven als twee hexadecimale getallen van 16 cijfers, of als twee decimale getallen van 19 cijfers. De getallen moeten worden gescheiden door een streepje, onderstrepingsteken of dubbele punt. Er moeten voorloopnullen worden toegevoegd als een van beide getallen onvoldoende cijfers heeft.

## Identity Service cookie

```
{
    namespace: "ECID",
    type: "standard",
    value: "00497781304058976192356650736267671594"
}
```

De waarde moet worden opgegeven als een decimaal getal van 38 cijfers. Als u dit getal haalt uit de twee mcvisid\_high/low- of post\_msvisid\_high/low-kolommen van een datafeed of een Data Warehouse-rapport, moet u elk van beide getallen met nullen aanvullen tot 19 cijfers en ze vervolgens aan elkaar schakelen met de hoogste waarde eerst.

Het is ook acceptabel om `"namespaceId": 4` te gebruiken in plaats van of in aanvulling op `"namespace": "ECID"`, en het kan zijn dat sommige andere Adobe-producten dit formulier gebruiken.

>[!NOTE]
>
>De Experience Cloud ID (ECID) werd vroeger de Marketing Cloud-id (MCID) genoemd en wordt nog steeds bij die naam genoemd in een deel van de bestaande documentatie.
>
>Deze id&#39;s zijn de enige id&#39;s die door Analytics worden ondersteund en die een andere “type”-waarde dan “analytics” gebruiken.

Als de indeling van het waardegedeelte van een van deze cookie-id&#39;s niet de indeling volgt die voor die id is beschreven, mislukt de Data Privacy-aanvraag met de fout “Waarde is niet correct opgemaakt”.

Deze cookie-id&#39;s worden doorgaans verzameld met het nieuwe [JavaScript voor privacy](https://developer.adobe.com/experience-platform-apis/references/privacy-service/). Dit biedt automatisch alle relevante code-/waardeparen voor deze JSON-id&#39;s.

Deze JavaScript-code vult de JSON in met andere code/waardeparen naast de bovenvermelde (naamruimte, type, waarde), maar de bovenvermelde velden zijn het belangrijkst voor de Analytics Data Privacy-verwerking, en de enige velden die u moet opgeven als u de id&#39;s op een andere manier verzamelt.

## Aangepaste bezoekers-id

```
{
     namespace: "customVisitorID",
     type: "analytics",
     value: "<ID>"
}
```

De naamruimte is ook vooraf gedefinieerd voor de aangepaste bezoekers-id.

## ID&#39;s in aangepaste variabelen

```
{
    namespace: "Email Address",
    type: "analytics", 
    value: "john@xyz.com" }, 
{
    namespace: "CRM ID", 
    type: "analytics", 
    value: "123456-ABCD" 
}
```

Voor id&#39;s in variabelen voor aangepaste traffic of conversie (props of eVars) geeft u de variabele een ID-DEVICE- of ID-PERSON-label en wijst u vervolgens uw eigen naamruimtenaam toe aan dat type id. Zie [Een naamruimte opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON.](gdpr-labels.md)

U kunt ook naamruimten zien die u eerder voor andere variabelen of rapportsuites hebt gedefinieerd en één daarvan opnieuw gebruiken, zodat dezelfde naamruimte gemakkelijk kan worden gebruikt voor al uw rapportsuites waarin dat type id wordt opgeslagen. Het is ook mogelijk om dezelfde naamruimte binnen een rapportsuite aan meerdere variabelen toe te wijzen. Zo slaan bijvoorbeeld sommige klanten een CRM-id op in een traffic variabele en een conversievariabele (afhankelijk van de pagina is het soms in de ene, soms in de andere, soms in allebei), en zij kunnen de naamruimte “CRM ID” aan beide variabelen toewijzen.

>[!TIP]
>
>Vermijd het gebruik van de friendly name van een variabele (de naam die wordt weergegeven in de rapportagegebruikersinterface) of het nummer van de variabele (zoals eVar12) wanneer u de naamruimte opgeeft in de Data Privacy-API, tenzij deze naamruimte is opgegeven bij het toepassen van het label ID-DEVICE of ID-PERSON. Door een naamruimte te gebruiken in plaats van een friendly name kan hetzelfde gebruikersidentiteitsblok de juiste variabele opgeven voor meerdere rapportsuites. Als de id bijvoorbeeld in sommige rapportsuites in verschillende eVars voorkomt, of als de friendly names niet overeenkomen (bijvoorbeeld wanneer de friendly name is gelokaliseerd voor een bepaalde rapportsuite).

>[!CAUTION]
>
>De naamruimten “visitorId” en “customVisitorId” zijn gereserveerd voor het identificeren van het verouderde Analytics-trackingcookie en de bezoekers-id van de Analytics-klant. Gebruik deze naamruimten niet voor variabelen voor aangepaste traffic of conversie.

Zie [Een naamruimte opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON.](/help/admin/c-data-governance/data-labeling/gdpr-labels.md)
