---
title: prop
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
feature: Appmeasurement Implementation
exl-id: 0d0ff8cd-1d8c-4263-866d-e51ad66148b0
role: Admin, Developer
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# prop

*Deze hulppagina beschrijft hoe te om steunen uit te voeren. Voor informatie over hoe de steunen als afmeting werken, zie [ steun ](/help/components/dimensions/prop.md) in de de gebruikersgids van Componenten.*

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken. Ze blijven niet bestaan na de treffer die ze zijn ingesteld.

>[!TIP]
>
>Adobe adviseert gebruikend [ eVars ](evar.md) in de meeste gevallen. In vorige versies van Adobe Analytics hadden props en eVars voor- en nadelen. Adobe heeft de eVars echter zodanig verbeterd dat ze nu bijna alle gevallen van gebruik voor props vervullen.

Als u het document van het oplossingsontwerp van a [&#128279;](/help/implement/prepare/solution-design.md) hebt, kunt u deze douanedimensies aan waarden toewijzen specifiek voor uw organisatie. Het aantal beschikbare props is afhankelijk van uw contract met Adobe. Er zijn maximaal 75 props beschikbaar als uw contract met Adobe dit ondersteunt.

## Proefversies met de Web SDK

Props worden toegewezen aan de volgende variabelen:

* [ voorwerp XDM ](/help/implement/aep-edge/xdm-var-mapping.md): `xdm._experience.analytics.customDimensions.props.prop1` - `xdm._experience.analytics.customDimensions.props.prop75` - de lijststeunen worden gespecificeerd in a [ afzonderlijke reeks gebieden ](#list-props-web-sdk).
* [ voorwerp van Gegevens ](/help/implement/aep-edge/data-var-mapping.md): `data.__adobe.analytics.prop1` - `data.__adobe.analytics.prop75`; of `data.__adobe.analytics.c1` - `data.__adobe.analytics.c75` - de lijstuitdrukkingen zijn inbegrepen in deze gebieden.

## Wordt gebruikt met de Adobe Analytics-extensie

U kunt eigenschappen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Login aan [ de Inzameling van Gegevens van Adobe Experience Platform ](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Klik op de gewenste tageigenschap.
3. Ga naar het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak een regel).
4. Klik onder [!UICONTROL Actions] op een bestaande [!UICONTROL Adobe Analytics - Set Variables] -actie of klik op het plusteken (+).
5. Stel de vervolgkeuzelijst [!UICONTROL Extension] in op Adobe Analytics en op [!UICONTROL Action Type] op [!UICONTROL Set Variables] .
6. Zoek de sectie [!UICONTROL Props] .

U kunt een eigenschap instellen op een waarde of een gegevenselement. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.prop1 - s.prop75 in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

Elke prop-variabele is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 100 bytes. De waarden langer dan 100 bytes worden automatisch afgebroken wanneer ze naar Adobe worden verzonden.

```js
s.prop1 = "Example custom value";
```

## Props weergeven

Keuzerondjes in de lijst zijn een instelling die wordt toegepast op profielen waarmee de variabele meerdere waarden in dezelfde hit kan bevatten. Als deze instelling niet is ingeschakeld of als het verkeerde scheidingsteken wordt gebruikt, wordt de variabele als één waarde behandeld.

### Lijsteigenschappen configureren

Laat lijststeunen in [ variabelen van het Verkeer ](/help/admin/tools/manage-rs/edit-settings/c-traffic-variables/traffic-var.md) onder de montages van de rapportreeks toe. Zorg ervoor dat het gewenste scheidingsteken correct wordt gevormd. Adobe heeft geen standaardscheidingsteken.

>[!TIP]
>
>Gemeenschappelijke scheidingstekens die in implementaties worden gebruikt zijn een komma (`,`), dubbelepunt (`:`), puntkomma (`;`), of pijp (`|`). U kunt elk niet-uitgebreid ASCII-scheidingsteken gebruiken dat het beste bij uw implementatie past.

### Lijsteigenschappen instellen met de Web SDK {#list-props-web-sdk}

Als het gebruiken van het [**voorwerp XDM**](/help/implement/aep-edge/xdm-var-mapping.md), worden de lijstuitdrukkingen in kaart gebracht aan `xdm._experience.analytics.customDimensions.listProps.prop1.values[]` - `xdm._experience.analytics.customDimensions.listProps.prop75.values[]`. SDK van het Web gebruikt automatisch het correcte die afbakening onder de montages van de rapportreeks wordt vermeld. Als u het scheidingsteken op het XDM gebied (bijvoorbeeld, `xdm._experience.analytics.customDimensions.props.prop1.delimiter`) plaatst, die het scheidingsteken met voeten treedt automatisch die uit de montages van de rapportreeks wordt teruggewonnen en tot onjuist het ontleden van het lijstkoord kan leiden.

Als het gebruiken van het [**gegevensvoorwerp**](/help/implement/aep-edge/data-var-mapping.md), gebruiken de lijststeunen de zelfde gebieden zoals standaardsteunen en volgen de syntaxis van AppMeasurement.

### Lijsteigenschappen instellen met de Adobe Analytics-extensie en AppMeasurement

Zodra u lijststeunen in de montages van de rapportreeks met het gewenste scheidingsteken vormt, zijn er geen implementatieverschillen behalve het gebruiken van het scheidingsteken.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

>[!IMPORTANT]
>
>Voor lijstprofielen geldt nog steeds de maximumlengte van 100 bytes. Lijstprofielen zijn eenvoudiger om deze limiet te bereiken en te worden afgekapt, omdat ze meerdere waarden kunnen bevatten. U kunt afkortingen of verkorte waarden gebruiken als deze limiet van 100 bytes wordt bereikt.

Als u dezelfde waarde meerdere keren instelt in een lijst-eigenschap, wordt de duplicatie ongedaan gemaakt in de rapportage. Analysis Workspace telt het aantal treffers waar een waarde wordt gezien, en niet het aantal tijden een waarde in gegevens bestaat.
