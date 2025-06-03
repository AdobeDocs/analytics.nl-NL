---
description: Het type bijhouden bepaalt hoe de Adobe Analytics-implementatie de gegevens van uw zoekmachine volgt. Dit type tekstspatiëring is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met zoekprogrammagegevens.
title: Type track
feature: Advertising Analytics
exl-id: 3e2ed26f-dfb2-43ea-8eb6-e332cd10fb29
source-git-commit: 6bedfb9b1333a442bf17cf71dad1e0883b97fd45
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 0%

---

# Type track

Het type bijhouden bepaalt hoe de Adobe Analytics-implementatie de gegevens van uw zoekmachine volgt. Dit type tekstspatiëring is een vereiste stap om de Adobe Analytics-gegevens correct aan te vullen met zoekprogrammagegevens.

<!--

Here is a video overview of how to implement the Advertising Analytics tracking template:

>[!VIDEO](https://video.tv.adobe.com/v/23120/?quality=12)

-->

Er worden twee traceringsmodi ondersteund: [!UICONTROL Auto] en [!UICONTROL Manual] .

## [!UICONTROL Auto] Tekstspatiëring {#concept_C4C6107838C947CFBB7F4E0CB94264F0}

Met [!UICONTROL Auto] tracking kan de Advertising Cloud-engine bepalen hoe de gegevens van de zoekmachine moeten worden verwerkt. Auto het volgen is de eenvoudigere benadering, maar kan niet in de beste geïntegreerde dataset resulteren.

Daarom moet u een selectievakje voor bevestiging inschakelen wanneer u **[!UICONTROL Auto]** selecteert voordat u de accountinstelling kunt opslaan.

Als u een zoekprogrammaaccount met **[!UICONTROL Auto]** type wilt configureren, bent u verantwoordelijk voor het uitvoeren van de volgende handelingen:

* De parameter `s_kwcid` en de waarde worden toegevoegd aan de sjablonen voor het bijhouden van accounts of de bestemmingspagina-URL&#39;s in de account die wordt toegevoegd. Deze parameter en waarde worden ingevoegd aan het einde van de URL. Mogelijk is aanvullende actie van uw kant vereist als uw webserver aan het einde van de URL een bepaald `key=value` paar nodig heeft. Of een update ter ondersteuning van een nieuw `key=value` -paar in de URL. Het is uw verantwoordelijkheid om ervoor te zorgen dat de toegevoegde URL-parameters correct blijven op de laatste bestemmingspagina.
* Daarnaast kunnen trefwoorden in de bestemmings-URL worden ingevoegd als onderdeel van de waarde `s_kwcid` . Bevestig dat uw webserver deze tekens kan ondersteunen als deze speciale tekens of symbolen bevatten. Een veel voorkomend speciaal teken is bijvoorbeeld `+` , dat wordt gebruikt in de trefwoorden &#39;Grote overeenkomst gewijzigd&#39;.

>[!IMPORTANT]
>
>Leer meer op of u de `s_kwcid` parameter aan uw [ Beleid van de Veiligheid van de Inhoud ](https://experienceleague.adobe.com/nl/docs/id-service/using/reference/csp) zou moeten toevoegen.

## Handmatig bijhouden {#concept_87B28BA9E7F84BA5972F69E6F3482A33}

Met handmatig bijhouden kunt u opgeven hoe het Advertising Analytics-gegevensintegratieproces de gegevens van de zoekmachine moet behandelen.

### Handmatige tracering toevoegen aan Google-account {#section_41C1EB1AEB034544A5BC291F53C05C67}

De tekenreeks die aan je Google-account moet worden toegevoegd, wordt hieronder weergegeven. U moet de tekenreeks toevoegen aan al uw trackingsjablonen die in uw account worden gebruikt.

>[!IMPORTANT]
>
>De *`<Advertising Analytics ID>`* waarde (in **gewaagd** hieronder) is generiek en **moet met uw specifiek koord van identiteitskaart van de rekening** worden vervangen. U kunt de id-tekenreeks van uw specifieke account ophalen vanuit het accountscherm onder de sectie [!UICONTROL Tracking] .

**het Volgen Koord voor Campagnes:**

```
s_kwcid=AL! 
<b><Advertising Analytics ID></b>!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

![ Google ](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/assets/google-account.png)

Voorbeelden van volgcodes in verschillende sjabloonindelingen voor reeksspatiëring:

**`{lpurl}`**

```
{lpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**`{lpurl}`met extra URL-parameter**

```
{lpurl}?campaign=PPC&s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!network}!{product_partition_id}!{keyword}
```

**derden (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

**derden (DoubleClick)`{lpurl}`**

Om ervoor te zorgen dat de tekenreeks doorloopt naar de URL van de laatste bestemmingspagina, moet u de tekenreeks voldoende coderen:

* als de URL een omleiding doorloopt, en
* gebruikt geen waarde voor unescape edlpurl.


```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}
```

### Handmatige tracering toevoegen aan Microsoft Advertising-account {#section_094F8ACA493C4D65B1F54A695558EBF2}

De tekenreeks die aan uw Microsoft Advertising-account moet worden toegevoegd, wordt hieronder weergegeven. U moet de tekenreeks toevoegen aan alle laatste URL-achtervoegsels die in uw account worden gebruikt.

>[!IMPORTANT]
>
>De _`<Advertising Analytics ID>`_waarde (in **gewaagd**&#x200B;hieronder) is generiek en **moet met uw specifiek koord van identiteitskaart van de rekening**&#x200B;worden vervangen. U kunt de id-tekenreeks van uw specifieke account ophalen vanuit het accountscherm onder de sectie &#39;Bijhouden&#39;.

**het Volgen Koord voor Campagnes:**

```
s_kwcid=AL!<Advertising Analytics ID>!10!{AdId}!{OrderItemId} 
```

![ voeg het volgen codeparameters ](/help/integrate/c-advertising-analytics/c-adanalytics-workflow/assets/bing-account.png) toe

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

**derden (DoubleClick)`{unescapedlpurl}`**

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={unescapedlpurl}?s_kwcid=AL!9999!10!{AdId}!{OrderItemId}
```

**derden (DoubleClick)`{lpurl}`**

Om ervoor te zorgen dat de tekenreeks doorloopt naar de URL van de laatste bestemmingspagina, moet u de tekenreeks voldoende coderen:

* als de URL een omleiding doorloopt, en
* gebruikt geen waarde voor unescape edlpurl.

```
https://clickserve.dartsearch.net/link/click?{_dssagcrid}&{_dssftfiid}&ds_e_adid={creative}&ds_e_matchtype={ifsearch:search}{ifcontent:content}&ds_e_device={device}&ds_e_network={network}&{ifpla:ds_e_product_group_id={product_partition_id}&ds_e_product_id={product_id}&ds_e_product_merchant_id={merchant_id}&ds_e_product_country={product_country}&ds_e_product_language={product_language}&ds_e_product_channel={product_channel}&ds_e_product_store_id={product_store_id}}&ds_url_v=2&ds_dest_url={lpurl}?s_kwcid%3DAL!9999!10!{AdId}!{OrderItemId}
```
