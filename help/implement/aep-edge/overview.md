---
title: Adobe Analytics implementeren met Adobe Experience Platform Edge
description: Overzicht van het gebruik van XDM-gegevens van Experience Platform in Adobe Analytics
exl-id: 7d8de761-86e3-499a-932c-eb27edd5f1a3
feature: Implementation Basics
role: Admin, Developer, Leader
source-git-commit: a515927313fdc6025fb3ff8eaedf0b3742bede70
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Adobe Analytics implementeren met de Adobe Experience Platform Edge Network

Met Adobe Experience Platform Edge Network kunt u gegevens die bestemd zijn voor meerdere producten naar een gecentraliseerde locatie verzenden. De Edge Network stuurt de juiste informatie door naar de gewenste producten. Met dit concept kunt u de implementatie-inspanningen consolideren, met name voor het overspannen van meerdere gegevensoplossingen. Adobe Analytics is een van de producten waarnaar u gegevens kunt verzenden via de Edge Network.

## Hoe Adobe Analytics Edge Network-gegevens verwerkt

Gegevens die naar Adobe Experience Platform Edge Network worden verzonden kunnen drie formaten volgen: **voorwerp XDM**, **voorwerp van Gegevens**, en **Contextgegevens**. Wanneer een gegevensstroom gegevens doorstuurt naar Adobe Analytics, worden ze omgezet in een indeling die Adobe Analytics kan verwerken.

## `xdm` -object

Vorm aan schema&#39;s die u baseert op [ XDM ](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=nl) (het Model van Gegevens van de Ervaring) creeert. XDM biedt u flexibiliteit in welke velden worden gedefinieerd als onderdeel van gebeurtenissen. Als u een vooraf bepaald schema specifiek voor Adobe Analytics wilt gebruiken, kunt u de [ groep van het het schemagebied van de ErvaringEvent van Adobe Analytics ](https://experienceleague.adobe.com/nl/docs/experience-platform/xdm/field-groups/event/analytics-full-extension) aan uw schema toevoegen. Nadat u het schema hebt toegevoegd, kunt u het `xdm` -object in de SDK Web gebruiken om gegevens naar een rapportsuite te verzenden. Wanneer gegevens op de Edge Network worden ontvangen, wordt het XDM-object omgezet in een indeling die Adobe Analytics begrijpt.

Zie [ XDM objecten veranderlijke afbeelding aan Adobe Analytics ](xdm-var-mapping.md) voor een volledige verwijzing van XDM gebieden en hoe zij aan de variabelen van Analytics in kaart brengen.

>[!TIP]
>
>Als u van plan bent om aan [ Customer Journey Analytics ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/cja-landing) in de toekomst te bewegen, adviseert Adobe tegen het gebruiken van de het schemagebiedgroep van Adobe Analytics. In plaats daarvan, adviseert Adobe [ creërend uw eigen schema ](https://experienceleague.adobe.com/nl/docs/analytics-platform/using/compare-aa-cja/upgrade-to-cja/schema/cja-upgrade-schema-architect) en gebruik datastream afbeelding om de gewenste variabelen van Analytics te bevolken. Deze strategie vergrendelt u niet op een schema van props en eVars wanneer u klaar bent om over te stappen naar Customer Journey Analytics.

## `data` -object

Als alternatief voor het gebruik van het object `xdm` kunt u in plaats daarvan het object `data` gebruiken. Het gegevensvoorwerp is gericht op implementaties die momenteel AppMeasurement gebruiken, die de verbetering aan het Web SDK veel gemakkelijker maken. De Edge Network detecteert de aanwezigheid van velden die specifiek zijn voor Adobe Analytics zonder dat een schema hoeft te worden gevolgd.

Zie [ objecten van Gegevens veranderlijke afbeelding aan Adobe Analytics ](data-var-mapping.md) voor een volledige verwijzing van gegevensobjecten gebieden en hoe zij aan de variabelen van Analytics in kaart brengen.

## Contextgegevensvariabelen

Verzend gegevens naar de Edge Network in elke gewenste indeling. Om het even welke gebieden die niet automatisch aan `xdm` of `data` objecten gebieden in kaart brengen zijn inbegrepen als [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) wanneer door:sturen aan Adobe Analytics. U moet [ regels van de Verwerking ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md) dan gebruiken om de gewenste gebieden aan hun respectieve variabelen van Analytics in kaart te brengen.

Stel dat u een aangepast XDM-schema had dat er als volgt uitziet:

```json
{
  "xdm": {
    "key": "value",
    "animal": {
      "species": "Raven",
      "size": "13 inches"
    },
    "array": [
      "v0",
      "v1",
      "v2"
    ],
    "objectArray":[{
      "ad1": "300x200",
      "ad2": "60x240",
      "ad3": "600x50"
    }]
  }
}
```

Dan zouden deze gebieden de sleutels van contextgegevens beschikbaar aan u in de interface van de Regels van de Verwerking zijn:

```javascript
a.x.key // value
a.x.animal.species // Raven
a.x.animal.size // 13 inches
a.x.array.0 // v0
a.x.array.1 // v1
a.x.array.2 // v2
a.x.objectarray.0.ad1 // 300x200
a.x.objectarray.1.ad2 // 60x240
a.x.objectarray.2.ad3 // 600x50
```
