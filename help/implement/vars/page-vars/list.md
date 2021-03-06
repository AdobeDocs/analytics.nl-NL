---
title: list
description: Aangepaste variabelen die meerdere waarden in dezelfde hit bevatten.
feature: Variables
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
source-git-commit: 9e20c5e6470ca5bec823e8ef6314468648c458d2
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---

# list

De variabelen van de lijst zijn douanevariabelen die u kunt gebruiken hoe u zou willen. Ze werken op dezelfde manier als Vars, maar ze kunnen meerdere waarden in dezelfde hit bevatten. Lijstvariabelen hebben geen tekenlimiet.

Zorg ervoor u registreert hoe u elke lijstvariabele en hun logica in uw gebruikt [document ontwerp oplossing](../../prepare/solution-design.md).

>[!NOTE]
>
>In lijstvariabelen worden de meest recente 250 waarden per bezoeker opgeslagen. Als er voor een bepaalde bezoeker meer dan 250 unieke waarden zijn, worden de oudste waarden niet aan metriek toegewezen.

## Lijstvariabelen instellen in de instellingen van de rapportsuite

Zorg ervoor dat u elke lijstvariabele in de montages van de rapportreeks vormt alvorens hen in uw implementatie te gebruiken. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/list-var-admin.md) in de handleiding Admin.

## Variabelen weergeven die de SDK van het web gebruiken

Lijstvariabelen zijn [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder de XDM-velden `_experience.analytics.customDimensions.lists.list1` tot `_experience.analytics.customDimensions.lists.list3`.

## Variabelen weergeven die de extensie Adobe Analytics gebruiken

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de douane code redacteur, na syntaxis AppMeasurement.

## s.list1 - s.list3 in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

Elke lijstvariabele is een koord dat douanewaarden specifiek voor uw organisatie bevat. Zij hebben geen maximum aantal bytes; elke individuele waarde heeft echter een maximum van 255 bytes. Het scheidingsteken dat u gebruikt wordt bepaald wanneer vestiging de variabele in de montages van de rapportreeks. Gebruik geen spaties bij het scheiden van meerdere items.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

>[!TIP]
>
>Als u dubbele waarden instelt in dezelfde hit, worden alle instanties van die waarden door Adobe gedupliceerd. Als u bijvoorbeeld `s.list1 = "Example,Example";`, wordt ????n exemplaar geteld in rapporten.

## Lijsproeven met lijstvariabelen vergelijken

De steunen van de lijst en lijstvariabelen kunnen allebei veelvoudige waarden in de zelfde slag bevatten. Er zijn echter verschillende belangrijke verschillen tussen deze twee typen variabelen.

* Elke eigenschap kan een lijst-eigenschap worden. U kunt in feite maximaal 75 lijstprofielen hebben, als elke eigenschap een lijst-eigenschap is. Er zijn slechts drie keuzelijsten beschikbaar.
* Keuzerondjes voor lijsten hebben een limiet van 100 bytes voor de gehele variabele. Lijstvariabelen hebben een limiet van 255 bytes per waarde en geen limiet voor het totale aantal bytes.
* Lijstprofielen blijven alleen behouden wanneer ze worden ingesteld. Lijstvariabelen hebben de gewenste vervalinstelling. Met [rapporttijdverwerking](/help/components/vrs/vrs-report-time-processing.md)kunt u aangepaste attributie toepassen op zowel lijsteigenschappen als lijstvariabelen.
