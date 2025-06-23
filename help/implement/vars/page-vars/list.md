---
title: list
description: Aangepaste variabelen die meerdere waarden in dezelfde hit bevatten.
feature: Appmeasurement Implementation
exl-id: 612f6f10-6b68-402d-abb8-beb6f44ca6ff
role: Admin, Developer
source-git-commit: 665bd68d7ebc08f0da02d93977ee0b583e1a28e6
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 0%

---

# list

De variabelen van de lijst zijn douanevariabelen die u kunt gebruiken hoe u zou willen. Ze werken op dezelfde manier als Vars, maar ze kunnen meerdere waarden in dezelfde hit bevatten. Lijstvariabelen hebben geen tekenlimiet.

Zorg ervoor dat u registreert hoe u elke lijstvariabele en hun logica in uw [ document van het oplossingsontwerp ](../../prepare/solution-design.md) gebruikt.

>[!NOTE]
>
>De variabelen van de lijst slaan de meest recente die waarden per bezoeker op zijn [!UICONTROL Max values] plaatsen in [ de reeksinstellingen van het Rapport ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) wordt gebaseerd. Er worden maximaal 250 waarden ondersteund. Als er meer unieke waarden zijn dan zijn toegestaan door de instelling [!UICONTROL Max values] , worden de oudste waarden niet aan metriek toegewezen.

## Lijstvariabelen instellen in de instellingen van de rapportsuite

Zorg ervoor dat u elke lijstvariabele in de montages van de rapportreeks vormt alvorens hen in uw implementatie te gebruiken. Zie [ variabelen van de Omzetting ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) in de gids Admin. Deze stap geldt voor alle implementatiemethoden.

## Variabelen weergeven die de Web SDK gebruiken

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), gebruiken de lijstvariabelen de gebieden XDM `xdm._experience.analytics.customDimensions.lists.list1.list[]` aan `xdm._experience.analytics.customDimensions.lists.list3.list[]`. Elk arrayelement bevat een `"value"` -object dat elke tekenreeks bevat. Er is geen behoefte om een afbakening te verstrekken; de servers van de gegevensinzameling van Adobe ontdekken automatisch en omvatten het correcte die afbakeningsteken in [ wordt geplaatst de reeksinstellingen van het Rapport ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md).

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
>Het Adobe XDM-schema bevat naast `value` -objecten in elke `list[]` -array ook `key` -objecten. Adobe gebruikt deze `key` -objecten niet bij het verzenden van gegevens naar Adobe Analytics.

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), gebruik van lijstvariabelen `data.__adobe.analytics.list1` - `data.adobe.analytics.list3` na de syntaxis van AppMeasurement. Zorg ervoor dat u het correcte die afbakeningsteken gebruikt in [ de reeksinstellingen van het Rapport ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md) wordt geplaatst.

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

Er is geen specifiek veld in de Adobe Analytics-extensie voor het gebruik van deze variabele. Gebruik de aangepaste code-editor volgens de AppMeasurement-syntaxis.

## s.list1 - s.list3 in AppMeasurement en de de redacteur van de de uitbreidingsdouane van de Analyse

Elke lijstvariabele is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. Deze variabele heeft geen maximum aantal bytes. Elke individuele waarde heeft echter een maximum aantal van 255 bytes. Het scheidingsteken dat u gebruikt wordt bepaald wanneer vestiging de variabele in [ de reeksinstellingen van het Rapport ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/conversion-var-admin/list-var-admin.md). Gebruik geen spaties bij het scheiden van meerdere items.

```js
// A list variable configured with a comma as a delimiter
s.list1 = "Example value 1,Example value 2,Example value 3";
```

>[!TIP]
>
>Als u dubbele waarden instelt in dezelfde hit, worden alle instanties van deze waarden door Adobe gededupliceerd. Als u bijvoorbeeld `s.list1 = "Brick,Brick";` instelt, wordt één instantie geteld in rapporten.

## Lijsproeven met lijstvariabelen vergelijken

De steunen van de lijst en lijstvariabelen kunnen allebei veelvoudige waarden in de zelfde slag bevatten. Er zijn echter verschillende belangrijke verschillen tussen deze twee variabeletypen.

* Elke eigenschap kan een lijst-eigenschap worden. U kunt in feite maximaal 75 lijstprofielen hebben, als elke eigenschap een lijst-eigenschap is. Er zijn slechts drie keuzelijsten beschikbaar.
* Keuzerondjes voor lijsten hebben een limiet van 100 bytes voor de gehele variabele. Lijstvariabelen hebben een limiet van 255 bytes per waarde en geen limiet voor het totale aantal bytes.
* Lijstprofielen blijven alleen behouden wanneer ze worden ingesteld. Lijstvariabelen hebben de gewenste vervalinstelling. Nochtans, met [ verwerking van de rapporttijd ](/help/components/vrs/vrs-report-time-processing.md), kunt u douaneattributie op zowel lijsteigenschappen als lijstvariabelen toepassen.
