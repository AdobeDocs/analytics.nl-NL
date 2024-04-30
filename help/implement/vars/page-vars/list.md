---
title: list
description: Aangepaste variabelen die meerdere waarden in dezelfde hit bevatten.
feature: Variables
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
role: Admin, Developer
source-git-commit: 7c8ffe8f4ccf0577136e4d7ee96340224897d2a4
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# list

De variabelen van de lijst zijn douanevariabelen die u kunt gebruiken hoe u zou willen. Ze werken op dezelfde manier als Vars, maar ze kunnen meerdere waarden in dezelfde hit bevatten. Lijstvariabelen hebben geen tekenlimiet.

Zorg ervoor dat u opneemt hoe u elke lijstvariabele en hun logica in uw [document ontwerp oplossing](../../prepare/solution-design.md).

>[!NOTE]
>
>In lijstvariabelen worden de meest recente waarden per bezoeker opgeslagen op basis van de [!UICONTROL Max values] instellen in [Instellingen van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md). Er worden maximaal 250 waarden ondersteund. Als er meer unieke waarden zijn dan de [!UICONTROL Max values] Met de instelling allow, worden de oudste waarden niet aan metriek toegewezen.

## Lijstvariabelen instellen in de instellingen van de rapportsuite

Zorg ervoor dat u elke lijstvariabele in de montages van de rapportreeks vormt alvorens hen in uw implementatie te gebruiken. Zie [Conversievariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) in de handleiding Admin. Deze stap geldt voor alle implementatiemethoden.

## Variabelen weergeven die de SDK van het web gebruiken

Als u de [**XDM-object**](/help/implement/aep-edge/xdm-var-mapping.md), gebruiken lijstvariabelen de XDM gebieden `xdm._experience.analytics.customDimensions.lists.list1.list[]` tot `xdm._experience.analytics.customDimensions.lists.list3.list[]`. Elk arrayelement bevat een `"value"` object dat elke tekenreeks bevat. Het is niet nodig een scheidingsteken te verstrekken; de servers van de gegevensinzameling van de Adobe ontdekken automatisch en omvatten het correcte die afbakening in [Instellingen van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md).

```json
"xdm": {
  "_experience": {
    "analytics": {
      "customDimensions": {
        "lists": {
          "list1": {
            "list": [
              {
                "value": "Example value 1"
              },
              {
                "value": "Example value 2"
              },
              {
                "value": "Example value 3"
              }
            ]
          }
        }
      }
    }
  }
}
```

>[!NOTE]
>
>Het Adobe XDM-schema bevat `key` objecten naast `value` objecten in elk `list[]` array. Adobe gebruikt deze `key` objecten bij het verzenden van gegevens naar Adobe Analytics.

Als u de [**gegevensobject**](/help/implement/aep-edge/data-var-mapping.md), gebruikt voor lijstvariabelen `data.__adobe.analytics.list1` - `data.adobe.analytics.list3` volgende AppMeasurement syntaxis. Gebruik het juiste scheidingsteken dat is ingesteld in [Instellingen van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md).

```json
"data": {
  "__adobe": {
    "analytics": {
      "list1": "Example value 1,Example value 2,Example value 3"
    }
  }
}
```

## Variabelen weergeven die de extensie Adobe Analytics gebruiken

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de syntaxis van het AppMeasurement.

## s.list1 - s.list3 in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

Elke lijstvariabele is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. Deze variabele heeft geen maximum aantal bytes. Elke individuele waarde heeft echter een maximum aantal van 255 bytes. Het scheidingsteken dat u gebruikt, wordt bepaald wanneer u de variabele instelt in [Instellingen van rapportsuite](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md). Gebruik geen spaties bij het scheiden van meerdere items.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

>[!TIP]
>
>Als u dubbele waarden instelt in dezelfde hit, worden met Adobe alle instanties van die waarden gedupliceerd. Als u bijvoorbeeld `s.list1 = "Brick,Brick";`, wordt één exemplaar geteld in rapporten.

## Lijsproeven met lijstvariabelen vergelijken

De steunen van de lijst en lijstvariabelen kunnen allebei veelvoudige waarden in de zelfde slag bevatten. Er zijn echter verschillende belangrijke verschillen tussen deze twee variabeletypen.

* Elke eigenschap kan een lijst-eigenschap worden. U kunt in feite maximaal 75 lijstprofielen hebben, als elke eigenschap een lijst-eigenschap is. Er zijn slechts drie keuzelijsten beschikbaar.
* Keuzerondjes voor lijsten hebben een limiet van 100 bytes voor de gehele variabele. Lijstvariabelen hebben een limiet van 255 bytes per waarde en geen limiet voor het totale aantal bytes.
* Lijstprofielen blijven alleen behouden wanneer ze worden ingesteld. Lijstvariabelen hebben de gewenste vervalinstelling. Met [rapporttijdverwerking](/help/components/vrs/vrs-report-time-processing.md)kunt u aangepaste attributie toepassen op zowel lijsteigenschappen als lijstvariabelen.
