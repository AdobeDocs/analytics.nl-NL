---
title: prop
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
feature: Variables
exl-id: 0d0ff8cd-1d8c-4263-866d-e51ad66148b0
source-git-commit: 6de20d2fbbab6ded6c92f0c6f3536671f4b2ae46
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# prop

*Deze Help-pagina beschrijft hoe u instructies kunt implementeren. Voor informatie over hoe de steunen als dimensie werken, zie [prop](/help/components/dimensions/prop.md) in de gebruikershandleiding van Componenten.*

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken. Ze blijven niet bestaan na de hit die ze zijn ingesteld.

>[!TIP]
>
>Adobe raadt u aan [eVars](evar.md) in de meeste gevallen. In vorige versies van Adobe Analytics hadden props en eVars voor- en nadelen. Adobe heeft de eVars echter in die mate verbeterd dat ze nu bijna alle gevallen van gebruik voor props vervullen.

Als u een [document ontwerp oplossing](/help/implement/prepare/solution-design.md)kunt u deze aangepaste afmetingen toewijzen aan waarden die specifiek zijn voor uw organisatie. Het aantal beschikbare props is afhankelijk van uw contract met Adobe. Er zijn maximaal 75 props beschikbaar als uw contract met Adobe dit ondersteunt.

## Proefpersonen die de SDK van het Web gebruiken

Props zijn [toegewezen voor Adobe Analytics](https://experienceleague.adobe.com/docs/analytics/implementation/aep-edge/variable-mapping.html) onder de XDM-velden `_experience.analytics.customDimensions.props.prop1` tot `_experience.analytics.customDimensions.props.prop75`. Lijstprofielen worden opgegeven in een aparte set velden.

## Wordt gebruikt met de Adobe Analytics-extensie

U kunt eigenschappen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste tageigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] vervolgkeuzelijst naar Adobe Analytics en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Props] sectie.

U kunt een eigenschap instellen op een waarde of een gegevenselement. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.prop1 - s.prop75 in AppMeasurement en de de redacteur van de de uitbreidingsdouanecode van de Analyse

Elke prop-variabele is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 100 bytes. waarden die langer zijn dan 100 bytes, worden automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
s.prop1 = "Example custom value";
```

## Props weergeven

Keuzerondjes in de lijst zijn een instelling die wordt toegepast op profielen waarmee de variabele meerdere waarden in dezelfde hit kan bevatten. Als deze instelling niet is ingeschakeld of als het verkeerde scheidingsteken wordt gebruikt, wordt de variabele als één waarde behandeld.

### Lijsteigenschappen configureren

Lijsteigenschappen inschakelen in [Verkeersvariabelen](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/c-traffic-variables/traffic-var.md) onder rapportsuite-instellingen. Zorg ervoor dat het gewenste scheidingsteken correct wordt gevormd. Adobe heeft geen standaardscheidingsteken.

>[!TIP]
>
>In implementaties worden vaak scheidingstekens gebruikt (`,`), dubbele punt (`:`), puntkomma (`;`) of pijp (`|`). U kunt elk niet-uitgebreid ASCII-scheidingsteken gebruiken dat het beste bij uw implementatie past.

### Lijsteigenschappen instellen met de Web SDK

Zodra u lijstproeven in de montages van de rapportreeks met het gewenste scheidingsteken vormt, zijn de lijststeunen in kaart gebracht voor Adobe Analytics onder `_experience.analytics.customDimensions.listProps.prop1.values[]` tot `_experience.analytics.customDimensions.listProps.prop75.values[]`. De SDK van het Web gebruikt automatisch het correcte scheidingsteken dat onder de montages van de rapportreeks wordt vermeld. Als u het scheidingsteken instelt in het XDM-veld (bijvoorbeeld `_experience.analytics.customDimensions.props.prop1.delimiter`), dat het scheidingsteken met voeten treedt dat automatisch uit de montages van de rapportreeks wordt teruggewonnen en tot onjuist het ontleden van het lijstpro koord kan leiden.

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
