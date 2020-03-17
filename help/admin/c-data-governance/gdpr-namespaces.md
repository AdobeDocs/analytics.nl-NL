---
description: Elke identiteitskaart die u wilt kunnen zoeken wordt toegewezen een namespace, die een douanekoord is dat die identiteitskaart in om het even welke variabele identificeert waar het over al uw rapportreeksen wordt gebruikt.
title: Naamruimten
uuid: cab61844-3209-4980-b14c-6859de777606
translation-type: tm+mt
source-git-commit: cf910f98a1921b7558a6614a9d0d69f8e4f855b4

---


# Naamruimten

Elke identiteitskaart die u wilt kunnen zoeken wordt toegewezen een namespace, die een douanekoord is dat die identiteitskaart in om het even welke variabele identificeert waar het over al uw rapportreeksen wordt gebruikt.

De naamruimte-tekenreeks wordt gebruikt om de velden te identificeren waarnaar u wilt zoeken wanneer u een id opgeeft als onderdeel van een verzoek om gegevensprivacy. Wanneer een privacyverzoek voor gegevens wordt ingediend, bevat het verzoek een JSON-sectie waarin de id&#39;s van de betrokkene zijn vermeld die voor het verzoek moeten worden gebruikt. Meerdere id&#39;s kunnen worden opgenomen als onderdeel van één aanvraag voor een betrokkene. De JSON bevat:

* Een naamruimte-veld dat de naamruimte-tekenreeks bevat.
* Een veld &quot;type&quot; dat voor de meeste Adobe Analytics-aanvragen de waarde &quot;analytics&quot; bevat.
* Een veld &quot;value&quot; met de id waarnaar Analytics moet zoeken in de gekoppelde naamruimtevariabelen van elk van uw rapportsuites.

Raadpleeg de [Experience Cloud Data Privacy API documentatie](https://www.adobe.io/apis/experienceplatform/gdpr/docs/alldocs.html#!api-specification/markdown/narrative/technical_overview/privacy_service_overview/privacy_service_overview.md) voor meer informatie.

## Cookie-id

Legacy Analytics Tracking Cookie, ook wel Adobe Analytics ID (AID) genoemd:

```
{
   namespace: "AAID",
   type: "standard",
   value: "2CCEEAE88503384F-1188000089CA"
}
```

De waarde moet worden opgegeven als twee hexadecimale getallen, gescheiden door een streepje. Alle hexadecimale cijfers die alfabetische karakters zijn moeten worden gespecificeerd gebruikend hogere letters. De hexadecimale waarden mogen geen voorloopnullen hebben (houd rekening met het verschil met dezelfde waarde die in de afgekeurde vorm is opgegeven, waarbij voorloopnullen zijn vereist).

Het is ook acceptabel om dit formulier te gebruiken `"namespaceId": 10` in plaats van of in aanvulling op `"namespace": "AAID"` en sommige andere Adobe-producten kunnen dit formulier gebruiken.

## Legacy Analytics Tracking Cookie: Vervangen formulier

```
{
   "namespace": "visitorId",
   "type": "analytics",
   "value": "2cceeae88503384f-00001188000089ca"
}
```

Vervangen formulier:

De waarde moet worden opgegeven als twee hexadecimale getallen van 16 cijfers of als twee decimale getallen van 19 cijfers. De getallen moeten worden gescheiden door een streepje, onderstrepingsteken of dubbele punt. Voorloopnullen moeten worden toegevoegd als een van beide getallen onvoldoende cijfers heeft.

## Identity Service Cookie

```
{
    namespace: "ECID",
    type: "standard",
    value: "00497781304058976192356650736267671594"
}
```

De waarde moet worden opgegeven als een decimaal getal van 38 cijfers. Als u dit aantal van twee mcvisid\_high/low of post\_msvisid\_high/low kolommen van een gegevensvoer of het rapport van het Pakhuis van Gegevens trekt, moet u nul stootkussen elk van de twee aantallen aan 19 cijfers en dan hen samenvoegen met de hoge waarde eerst.

Het is ook aanvaardbaar om te gebruiken: in `"namespaceId": 4` plaats van of als aanvulling op `"namespace": "ECID"` en sommige andere Adobe-producten kunnen dat formulier gebruiken.

> [!NOTE] De Experience Cloud ID (ECID) werd voorheen de Marketing Cloud ID (MCID) genoemd en wordt nog steeds door die naam vermeld in een aantal bestaande documentatie.
>
>Deze id&#39;s zijn de enige id&#39;s die door Analytics worden ondersteund en die een andere waarde dan &quot;analytics&quot; gebruiken.

Als de indeling van het waardegedeelte van een van deze cookie-id&#39;s niet de indeling volgt die voor die id is beschreven, mislukt de aanvraag Gegevensprivacy, met de fout &quot;Waarde is niet correct opgemaakt&quot;.

Deze cookie-id&#39;s worden doorgaans verzameld met de nieuwe JavaScript [voor](https://www.adobe.io/apis/cloudplatform/gdpr/services/allservices.htm)privacy. Deze JavaScriptbiedt automatisch alle relevante sleutel-/waardeparen voor deze JSON-id&#39;s.

Deze JavaScript-code vult de JSON met andere sleutel/waardeparen in, naast de bovenstaande (naamruimte, type, waarde), maar de bovenstaande velden zijn het belangrijkst voor de verwerking van de Privacy van analysegegevens en de enige velden die u moet opgeven als u de id&#39;s op een andere manier verzamelt.

## Aangepaste bezoeker-id

```
{
     namespace: "customVisitorID",
     type: "analytics",
     value: "<ID>"
}
```

De naamruimte is ook vooraf gedefinieerd voor de aangepaste bezoeker-id.

## Id&#39;s in aangepaste variabelen

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

Voor id&#39;s in variabelen voor aangepast verkeer of conversie (props of eVars) geeft u aan dat de variabele een label voor ID-DEVICE of ID-PERSON heeft en wijst u vervolgens uw eigen naamruimtenaam toe aan dat type id. Zie Een naamruimte [opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON.](gdpr-labels.md)

U kunt ook namespaces zien die u eerder voor andere variabelen of rapportreeksen hebt bepaald en één van die opnieuw gebruiken, zodat zelfde namespace voor al uw rapportreeksen gemakkelijk kan worden gebruikt die dat type van identiteitskaart opslaan. Het is ook mogelijk om zelfde namespace aan veelvoudige variabelen binnen een rapportreeks toe te wijzen. Bijvoorbeeld, slaan sommige klanten identiteitskaart van CRM in een verkeersvariabele en een omzettingsvariabele op (afhankelijk van de pagina, is het soms in één of ander of allebei), en zij konden namespace &quot;identiteitskaart van CRM&quot;aan beide variabelen toewijzen.

> [!TIP] Vermijd het gebruik van de vriendelijke naam van een variabele (de naam die wordt weergegeven in de rapportage-UI) of het nummer van de variabele (zoals eVar12) wanneer u de naamruimte opgeeft voor de Data Privacy API, tenzij dit de naamruimte is die is opgegeven bij het toepassen van het label ID-DEVICE of ID-PERSON. Het gebruiken van namespace eerder dan een vriendschappelijke naam staat het zelfde blok van de gebruikersidentiteit toe om de correcte variabele voor veelvoudige rapportreeksen te specificeren. Bijvoorbeeld, als identiteitskaart in verschillende eVars in sommige van de rapportreeksen is, of als de vriendschappelijke namen niet aanpassen (zoals wanneer de vriendschappelijke naam voor een specifieke rapportreeks is gelokaliseerd).

> [!CAUTION] De naamruimten &quot;bezoekerId&quot; en &quot;customVisitorId&quot; zijn gereserveerd voor het identificeren van het verouderde cookie voor bijhouden van analysemogelijkheden en de bezoeker-id van de Analytics-klant. Gebruik deze naamruimten niet voor variabelen voor aangepast verkeer of conversie.

Zie Een naamruimte [opgeven wanneer u een variabele labelt als ID-DEVICE of ID-PERSON voor meer informatie.](/help/admin/c-data-governance/gdpr-labels.md)
