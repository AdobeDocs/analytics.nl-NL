---
description: Elke id die u wilt kunnen zoeken, krijgt een naamruimte toegewezen, een aangepaste tekenreeks die deze id identificeert in elke variabele waarin deze wordt gebruikt in al uw rapportsuites.
title: Naamruimten
feature: Data Governance
role: Admin
exl-id: 421572c2-2789-48bc-b530-d48216799724
source-git-commit: 325a42c080290509309e90c9127138800d5ac496
workflow-type: tm+mt
source-wordcount: '896'
ht-degree: 80%

---

# Naamruimten

Elke id die u wilt kunnen zoeken, krijgt een naamruimte toegewezen, een aangepaste tekenreeks die deze id identificeert in elke variabele waarin deze wordt gebruikt in al uw rapportsuites.

De naamruimtetekenreeks wordt gebruikt om velden te identificeren die u wilt doorzoeken wanneer u een id opgeeft als onderdeel van een Data Privacy-aanvraag. Wanneer een verzoek van de Privacy van Gegevens wordt voorgelegd, zal het verzoek een sectie JSON omvatten die de Onderwerp IDs specificeert van Gegevens voor het verzoek te gebruiken. Meerdere id&#39;s kunnen worden opgenomen als onderdeel van één aanvraag voor een betrokkene. De JSON bevat het volgende:

* Een naamruimteveld met de naamruimtetekenreeks.
* Een typeveld dat voor de meeste Adobe Analytics-aanvragen de waarde “analytics” bevat.
* Een “value”-veld met de id waarnaar Analytics moet zoeken in de gekoppelde naamruimtevariabelen van al uw rapportsuites.

Verwijs naar de [ documentatie van de Privacy API van de Gegevens van Experience Cloud ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/overview.html?lang=nl-NL) voor meer details en a [ lijst van standaard identiteitsnamespaces ](https://experienceleague.adobe.com/nl/docs/experience-platform/privacy/api/appendix#standard-namespaces). Zie [ een toegang/schrappingsbaan ](https://experienceleague.adobe.com/nl/docs/experience-platform/privacy/api/privacy-jobs#access-delete) voor een steekproefverzoek creëren.

## Cookie-id

Verouderd Analytics-trackingcookie, ook wel Adobe Analytics-id (AAID) genoemd:

```json
{
   "namespace": "AAID",
   "type": "standard",
   "value": "2CCEEAE88503384F-1188000089CA"
}
```

De waarde moet worden opgegeven als twee hexadecimale getallen, gescheiden door een streepje. Alle hexadecimale cijfers die alfabetische tekens zijn, moeten worden opgegeven in hoofdletters. De hexadecimale waarden mogen geen voorloopnullen hebben (houd rekening met het verschil met dezelfde waarde in de afgeschafte vorm, waarbij voorloopnullen zijn vereist).

Het is ook acceptabel om `"namespaceId": 10` te gebruiken in plaats van of in aanvulling op `"namespace": "AAID"`, en het kan zijn dat sommige andere Adobe-producten dit formulier gebruiken.

## Verouderde cookie voor analyse bijhouden: verouderd formulier

```json
{
   "namespace": "visitorId",
   "type": "analytics",
   "value": "2cceeae88503384f-00001188000089ca"
}
```

De waarde moet worden opgegeven als twee hexadecimale getallen van 16 cijfers, of als twee decimale getallen van 19 cijfers. De getallen moeten worden gescheiden door een streepje, onderstrepingsteken of dubbele punt. Er moeten voorloopnullen worden toegevoegd als een van beide getallen onvoldoende cijfers heeft.

## Cookie Identiteitsservice

```json
{
   "namespace": "ECID",
   "type": "standard",
   "value": "00497781304058976192356650736267671594"
}
```

De waarde moet worden opgegeven als een decimaal getal van 38 cijfers. Als u dit getal haalt uit de twee mcvisid\_high/low- of post\_msvisid\_high/low-kolommen van een datafeed of een Data Warehouse-rapport, moet u elk van beide getallen met nullen aanvullen tot 19 cijfers en ze vervolgens aan elkaar schakelen met de hoogste waarde eerst.

Het is ook acceptabel om `"namespaceId": 4` te gebruiken in plaats van of in aanvulling op `"namespace": "ECID"`, en het kan zijn dat sommige andere Adobe-producten dit formulier gebruiken.

>[!NOTE]
>
>De Experience Cloud-id (ECID) werd voorheen de Marketing Cloud-id (MCID) genoemd en wordt nog steeds door die naam vermeld in een aantal bestaande documentatie.
>
>Deze id&#39;s zijn de enige id&#39;s die door Analytics worden ondersteund en die een andere “type”-waarde dan “analytics” gebruiken.

Als de indeling van het waardegedeelte van een van deze cookie-id&#39;s niet de indeling volgt die voor die id is beschreven, mislukt de Data Privacy-aanvraag met de fout “Waarde is niet correct opgemaakt”.

Deze cookie-id&#39;s worden doorgaans verzameld met het nieuwe [JavaScript voor privacy](https://developer.adobe.com/experience-platform-apis/references/privacy-service/). Dit biedt automatisch alle relevante code-/waardeparen voor deze JSON-id&#39;s.

Deze JavaScript-code vult de JSON in met andere code/waardeparen naast de bovenvermelde (naamruimte, type, waarde), maar de bovenvermelde velden zijn het belangrijkst voor de Analytics Data Privacy-verwerking, en de enige velden die u moet opgeven als u de id&#39;s op een andere manier verzamelt.

## Aangepaste bezoekers-id

```json
{
    "namespace": "customVisitorID",
    "type": "analytics",
    "value": "<ID>"
}
```

De naamruimte is ook vooraf gedefinieerd voor de aangepaste bezoekers-id.

## ID&#39;s in aangepaste variabelen

```json
{
"namespace":"Email Address",
"type": "analytics", 
"value": "john@xyz.com" 
}, 
{
    "namespace": "CRM ID", 
    "type": "analytics",
    "value": "123456-ABCD" 
}
```

Voor id&#39;s in variabelen voor aangepaste traffic of conversie (props of eVars) geeft u de variabele een ID-DEVICE- of ID-PERSON-label en wijst u vervolgens uw eigen naamruimtenaam toe aan dat type id. Zie [Een naamruimte opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON.](/help/admin/tools/privacy-labeling/labels.md)

U kunt ook naamruimten zien die u eerder voor andere variabelen of rapportsuites hebt gedefinieerd en één daarvan opnieuw gebruiken, zodat dezelfde naamruimte gemakkelijk kan worden gebruikt voor al uw rapportsuites waarin dat type id wordt opgeslagen. Het is ook mogelijk om dezelfde naamruimte binnen een rapportsuite aan meerdere variabelen toe te wijzen. Zo slaan bijvoorbeeld sommige klanten een CRM-id op in een traffic variabele en een conversievariabele (afhankelijk van de pagina is het soms in de ene, soms in de andere, soms in allebei), en zij kunnen de naamruimte “CRM ID” aan beide variabelen toewijzen.

>[!TIP]
>
>Vermijd het gebruik van de vriendelijke naam van een variabele (de naam die wordt weergegeven in de rapportage-UI) of het nummer van de variabele (zoals eVar12) bij het opgeven van de naamruimte op de Data Privacy API, tenzij dit de naamruimte is die is opgegeven bij het toepassen van het label ID-DEVICE of ID-PERSON. Door een naamruimte te gebruiken in plaats van een friendly name kan hetzelfde gebruikersidentiteitsblok de juiste variabele opgeven voor meerdere rapportsuites. Als de id bijvoorbeeld in sommige rapportsuites in verschillende eVars voorkomt, of als de friendly names niet overeenkomen (bijvoorbeeld wanneer de friendly name is gelokaliseerd voor een bepaalde rapportsuite).

>[!CAUTION]
>
>De naamruimten `visitorId` en `customVisitorId` zijn gereserveerd voor het identificeren van de oude cookie voor bijhouden van analysemogelijkheden en de bezoeker-id van de Analyse-klant. Gebruik deze naamruimten niet voor variabelen voor aangepaste traffic of conversie.

Zie [Een naamruimte opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON.](/help/admin/tools/privacy-labeling/labels.md)
