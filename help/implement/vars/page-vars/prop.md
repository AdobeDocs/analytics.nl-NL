---
title: prop
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
feature: Variables
exl-id: 0d0ff8cd-1d8c-4263-866d-e51ad66148b0
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# prop

*Deze Help-pagina beschrijft hoe u instructies kunt implementeren. Voor informatie over hoe de steunen als dimensie werken, zie [prop](/help/components/dimensions/prop.md) in de gebruikershandleiding van Componenten.*

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken. Ze blijven niet bestaan na de hit die ze zijn ingesteld.

>[!TIP]
>
>Adobe raadt u aan [eVars](evar.md) in de meeste gevallen. In vorige versies van Adobe Analytics hadden props en eVars voor- en nadelen. Adobe heeft echter verbeteringen doorgevoerd in de mate waarin ze bijna alle gevallen van gebruik voor props naleven.

Als u een [document ontwerp oplossing](/help/implement/prepare/solution-design.md)kunt u deze aangepaste afmetingen toewijzen aan waarden die specifiek zijn voor uw organisatie. Het aantal beschikbare props is afhankelijk van uw contract met Adobe. Er zijn maximaal 75 props beschikbaar als uw contract met Adobe dit ondersteunt.

## Props met tags in Adobe Experience Platform

U kunt eigenschappen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar de [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
4. Onder [!UICONTROL Actions]klikt u op een bestaande [!UICONTROL Adobe Analytics - Set Variables] of klik op het pictogram &#39;+&#39;.
5. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] tot [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Props] sectie.

U kunt een eigenschap instellen op een waarde of een gegevenselement. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.prop1 - s.prop75 in AppMeasurement en de douane redacteur van de code

Elke prop-variabele is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 100 bytes. waarden die langer zijn dan 100 bytes, worden automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
s.prop1 = "Example custom value";
```

## Props weergeven

Keuzerondjes in de lijst zijn een instelling die wordt toegepast op profielen waarmee de variabele meerdere waarden in dezelfde hit kan bevatten. Als deze instelling niet is ingeschakeld of als het verkeerde scheidingsteken wordt gebruikt, wordt de variabele als één waarde behandeld.

### Lijsteigenschappen configureren

Schakel lijsteigenschappen in de instellingen van de rapportsuite in. Zie [Verkeersvariabelen](/help/admin/admin/c-traffic-variables/traffic-var.md) in de handleiding voor Admin-gebruikers. Zorg ervoor dat het gewenste scheidingsteken correct wordt gevormd. Adobe heeft geen standaardscheidingsteken.

>[!TIP]
>
>In implementaties worden vaak scheidingstekens gebruikt (`,`), dubbele punt (`:`), puntkomma (`;`) of pijp (`|`). U kunt elk scheidingsteken gebruiken dat het beste bij uw implementatie past.

### Lijsteigenschappen instellen

Zodra u lijststeunen in de montages van de rapportreeks met het gewenste scheidingsteken vormt, zijn er geen implementatieverschillen behalve het gebruiken van het scheidingsteken.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

>[!IMPORTANT]
>
>Voor lijstprofielen geldt nog steeds de maximumlengte van 100 bytes. Lijstprofielen zijn eenvoudiger om deze limiet te bereiken en te worden afgekapt, omdat ze meerdere waarden kunnen bevatten. U kunt afkortingen of verkorte waarden gebruiken als deze limiet van 100 bytes wordt bereikt.

Als u dezelfde waarde meerdere keren instelt in een lijst-eigenschap, wordt de duplicatie ongedaan gemaakt in de rapportage. Analysis Workspace telt het aantal treffers waar een waarde wordt gezien, en niet het aantal tijden een waarde in gegevens bestaat.
