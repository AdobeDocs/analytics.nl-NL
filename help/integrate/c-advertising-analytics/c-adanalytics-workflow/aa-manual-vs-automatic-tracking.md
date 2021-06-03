---
description: Het volgen bepaalt hoe de gegevens van de Motor van het Onderzoek door uw implementatie van Adobe Analytics worden gevolgd. Dit is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met de zoekengine-gegevens.
title: Handmatige modus voor bijhouden en Automatische modus
exl-id: 3e2ed26f-dfb2-43ea-8eb6-e332cd10fb29
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 1%

---

# Tracking: handmatige modus en automatische modus

Het volgen bepaalt hoe de gegevens van de Motor van het Onderzoek door uw implementatie van Adobe Analytics worden gevolgd. Dit is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met de zoekengine-gegevens.

Twee traceringsmodi worden ondersteund: Automatische modus en Handmatige modus.

## Automatisch bijhouden {#concept_C4C6107838C947CFBB7F4E0CB94264F0}

In de modus Automatisch kunt u bepalen hoe de gegevens van de zoekmachine moeten worden verwerkt door de Advertising Cloud-engine. Dit is de eenvoudigere benadering, maar het kan niet in de beste geïntegreerde dataset resulteren.

Als u Automatische modus selecteert, moet u daarom een selectievakje voor een bevestiging inschakelen voordat u de accountinstelling kunt opslaan.

Als u een account voor een zoekmachine wilt configureren in de modus Automatisch, bent u verantwoordelijk voor het uitvoeren van de volgende handelingen:

* De parameter en de waarde `s_kwcid` worden toegevoegd aan de sjablonen voor het bijhouden van accounts of aan de URL&#39;s van de landingspagina in de account die wordt toegevoegd. Deze wordt aan het einde van de URL ingevoegd. Aanvullende actie is mogelijk vereist van uw kant als uw webserver een bepaald sleutelwaardepaar aan het einde van de URL vereist OF een update ter ondersteuning van een nieuw sleutelwaardepaar in de URL. **Het is uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina.**
* Daarnaast kunnen trefwoorden in de bestemmings-URL worden ingevoegd als onderdeel van de waarde `s_kwcid`. Bevestig dat uw webserver deze tekens kan ondersteunen als deze speciale tekens of symbolen bevatten. Voorbeeld: Een veel voorkomend speciaal teken is &quot;+&quot;. Dit wordt gebruikt in de trefwoorden &quot;Uitgebreide overeenkomst gewijzigd&quot;.

>[!IMPORTANT]
>
>Leer meer op of u `s_kwcid` parameter aan uw [Beleid van de Veiligheid van de Inhoud ](https://experienceleague.adobe.com/docs/id-service/using/reference/csp.html) zou moeten toevoegen.

## Handmatige modus bijhouden {#concept_87B28BA9E7F84BA5972F69E6F3482A33}

In de modus Handmatig moet u opgeven hoe de gegevens van de zoekmachine moeten worden verwerkt door het Advertising Analytics-proces voor gegevensintegratie.

### Handmatig bijhouden toevoegen aan Google-account {#section_41C1EB1AEB034544A5BC291F53C05C67}

De tekenreeks die aan uw Google-account moet worden toegevoegd, wordt hieronder weergegeven. U moet de tekenreeks toevoegen aan al uw trackingsjablonen die in uw account worden gebruikt.

>[!IMPORTANT]
>
>De `<Advertising Analytics ID>`-waarde (in **bold** hieronder) is algemeen en **moet worden vervangen door de id-tekenreeks van uw specifieke account**. U kunt de id-tekenreeks van uw specifieke account ophalen vanuit het scherm voor het instellen van de account onder de sectie &#39;Bijhouden&#39;.

**Tekenreeks voor campagnes:**

```
s_kwcid=AL! 
<b><Advertising Analytics ID></b>!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

![](assets/Google.png)

Voorbeelden van volgcodes in verschillende sjabloonindelingen voor reeksspatiëring:

**`{lpurl}`**

```
{lpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**`{lpurl}`met extra URL-parameter**

```
{lpurl}?campaign=PPC&s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**Andere leverancier (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

**Andere leverancier (DoubleClick)`{lpurl}`**

Als de URL een omleiding doorloopt en geen &quot;unescape edlpurl&quot;-waarde gebruikt, moet u de tekenreeks voldoende keer coderen zodat deze doorloopt in de omleiding naar de laatste bestemmingspagina-URL.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

### Handmatig bijhouden toevoegen aan bankrekening {#section_094F8ACA493C4D65B1F54A695558EBF2}

De tekenreeks die aan uw Bing-account moet worden toegevoegd, wordt hieronder weergegeven. U moet de tekenreeks toevoegen aan alle laatste URL-achtervoegsels die in uw account worden gebruikt.

>[!IMPORTANT]
>
>De `<Advertising Analytics ID>`-waarde (in **bold** hieronder) is algemeen en **moet worden vervangen door de id-tekenreeks van uw specifieke account**. U kunt de id-tekenreeks van uw specifieke account ophalen vanuit het scherm voor het instellen van de account onder de sectie &#39;Bijhouden&#39;.

**Tekenreeks voor campagnes:**

```
s_kwcid=AL!<Advertising Analytics ID>!10!{AdId}!{OrderItemId} 
```

![](assets/Bing.png)

Voorbeelden van volgcodes in verschillende uiteindelijke indelingen voor URL-achtervoegsels:

**{lpurl}**

```
{lpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**`{lpurl}`met extra URL-parameter**

```
{lpurl}?campaign=PPC&
s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**Andere leverancier (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**Andere leverancier (DoubleClick)`{lpurl}`**

Als de URL een omleiding doorloopt en geen &quot;unescape edlpurl&quot;-waarde gebruikt, moet u de tekenreeks voldoende keer coderen zodat deze doorloopt in de omleiding naar de laatste bestemmingspagina-URL.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!10!{AdId}!{OrderItemId}
```
