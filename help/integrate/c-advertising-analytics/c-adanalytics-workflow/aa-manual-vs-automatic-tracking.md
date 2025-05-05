---
description: Het type bijhouden bepaalt hoe de Adobe Analytics-implementatie de gegevens van uw zoekmachine volgt. Dit type tekstspatiëring is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met zoekprogrammagegevens.
title: Type track
feature: Advertising Analytics
exl-id: 3e2ed26f-dfb2-43ea-8eb6-e332cd10fb29
source-git-commit: 243da53fda562c856d95db0f6d13b7ee1a9adae5
workflow-type: tm+mt
source-wordcount: '561'
ht-degree: 0%

---

# Type track

Het type bijhouden bepaalt hoe de Adobe Analytics-implementatie de gegevens van uw zoekmachine volgt. Dit type tekstspatiëring is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met zoekprogrammagegevens.

<!--

Here is a video overview of how to implement the Advertising Analytics tracking template:

>[!VIDEO](https://video.tv.adobe.com/v/23120/?quality=12)

-->

Twee traceringsmodi worden ondersteund: [!UICONTROL Auto] en [!UICONTROL Manual].

## [!UICONTROL Auto] Tekstspatiëring {#concept_C4C6107838C947CFBB7F4E0CB94264F0}

[!UICONTROL Auto] Door het bijhouden van tags kan de Advertising Cloud-engine bepalen hoe de gegevens van de zoekmachine moeten worden verwerkt. Auto het volgen is de eenvoudigere benadering, maar kan niet in de beste geïntegreerde dataset resulteren.

Dientengevolge moet u een bevestigingscheckbox controleren wanneer u selecteert **[!UICONTROL Auto]** voordat u de accountinstelling kunt opslaan.

Merk op dat om een rekening van de onderzoeksmotor met te vormen **[!UICONTROL Auto]** typt, bent u verantwoordelijk voor het nemen van de volgende acties:

* De `s_kwcid` parameter en waarde worden toegevoegd aan de sjablonen voor het bijhouden van accounts of de bestemmingspagina-URL&#39;s in de account die wordt toegevoegd. Deze parameter en waarde worden ingevoegd aan het einde van de URL. Mogelijk is aanvullende actie van uw kant vereist als uw webserver een bepaalde `key=value` paar aan het einde van de URL. Of een update ter ondersteuning van nieuwe `key=value` paar in URL. Het is uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina.
* Daarnaast kunnen trefwoorden in de bestemmings-URL worden ingevoegd als onderdeel van de `s_kwcid` waarde. Bevestig dat uw webserver deze tekens kan ondersteunen als deze speciale tekens of symbolen bevatten. Een gemeenschappelijk speciaal teken is bijvoorbeeld `+`, die wordt gebruikt in de trefwoorden &#39;Uitgebreide overeenkomst gewijzigd&#39;.

>[!IMPORTANT]
>
>Meer informatie over het toevoegen van de `s_kwcid` parameter aan uw [Beveiligingsbeleid voor inhoud](https://experienceleague.adobe.com/nl/docs/id-service/using/reference/csp).

## Handmatig bijhouden {#concept_87B28BA9E7F84BA5972F69E6F3482A33}

Met handmatig bijhouden kunt u opgeven hoe het Advertising Analytics-gegevensintegratieproces de gegevens van de zoekmachine moet behandelen.

### Handmatige tracering toevoegen aan Google-account {#section_41C1EB1AEB034544A5BC291F53C05C67}

De tekenreeks die aan je Google-account moet worden toegevoegd, wordt hieronder weergegeven. U moet de tekenreeks toevoegen aan al uw trackingsjablonen die in uw account worden gebruikt.

>[!IMPORTANT]
>
>De *`<Advertising Analytics ID>`* waarde (in **vet** is algemeen en **moet worden vervangen door de id-tekenreeks van uw specifieke account**. U kunt de id-tekenreeks van uw specifieke account ophalen vanuit het accountscherm onder de [!UICONTROL Tracking] sectie.

**Tekenreeks voor campagnes:**

```
s_kwcid=AL! 
<b><Advertising Analytics ID></b>!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

![Google](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/assets/google-account.png)

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

Om ervoor te zorgen dat de tekenreeks doorloopt naar de URL van de laatste bestemmingspagina, moet u de tekenreeks voldoende coderen:

* als de URL een omleiding doorloopt, en
* gebruikt geen waarde voor unescape edlpurl.


```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

### Handmatige tracering toevoegen aan bankaccount {#section_094F8ACA493C4D65B1F54A695558EBF2}

De tekenreeks die aan uw Bing-account moet worden toegevoegd, wordt hieronder weergegeven. U moet de tekenreeks toevoegen aan alle laatste URL-achtervoegsels die in uw account worden gebruikt.

>[!IMPORTANT]
>
>De _`<Advertising Analytics ID>`_waarde (in **vet**&#x200B;is algemeen en **moet worden vervangen door de id-tekenreeks van uw specifieke account**. U kunt de id-tekenreeks van uw specifieke account ophalen vanuit het accountscherm onder de sectie &#39;Bijhouden&#39;.

**Tekenreeks voor campagnes:**

```
s_kwcid=AL!<Advertising Analytics ID>!10!{AdId}!{OrderItemId} 
```

![Bing](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/assets/bing-account.png)

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

Om ervoor te zorgen dat de tekenreeks doorloopt naar de URL van de laatste bestemmingspagina, moet u de tekenreeks voldoende coderen:

* als de URL een omleiding doorloopt, en
* gebruikt geen waarde voor unescape edlpurl.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!10!{AdId}!{OrderItemId}
```
