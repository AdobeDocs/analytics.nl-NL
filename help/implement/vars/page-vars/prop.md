---
title: prop
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
translation-type: tm+mt
source-git-commit: ddab63a4fe3b8f1a3187893eba1ac3a1eda3bc41

---


# prop

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken.

> [!TIP] Adobe raadt u in de meeste gevallen aan eVars te gebruiken. In eerdere versies van Adobe Analytics hadden props en eVars voor- en nadelen voor elkaar. Adobe heeft echter verbeteringen aangebracht in Vars waarin vrijwel alle gevallen van gebruik voor props zijn opgenomen. Zie [Vars](evar.md) voor een eigenschapvergelijking tussen deze twee types van douanevariabele.

Als uw organisatie steunt gebruikt, zorg ervoor u hun gebruik en logica in uw document [van het](../../prepare/solution-design.md)oplossingsontwerp registreert.

## Props in Adobe Experience Platform Launch

U kunt eigenschappen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Props] sectie.

U kunt een eigenschap selecteren om een waarde of gegevenselement in te stellen. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.prop1 - s.prop75 in AppMeasurement en Launch de redacteur van de douanecode

Elke prop-variabele is een tekenreeks die aangepaste waarden bevat die specifiek zijn voor uw organisatie. De maximale lengte is 100 bytes. Als waarden langer zijn dan 100 bytes, worden deze automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
s.prop1 = "Example custom value";
```

## Props weergeven

Keuzerondjes in de lijst zijn een instelling die wordt toegepast op profielen waarmee de variabele meerdere waarden in dezelfde hit kan bevatten. Als deze instelling niet is ingeschakeld of als het verkeerde scheidingsteken wordt gebruikt, wordt de variabele als één waarde behandeld.

### Lijsteigenschappen configureren

Schakel lijsteigenschappen in de instellingen van de rapportsuite in. Zie [Verkeersvariabelen](/help/admin/admin/c-traffic-variables/traffic-var.md) in de gebruikershandleiding Admin. Zorg ervoor dat het gewenste scheidingsteken correct wordt gevormd. Adobe heeft geen standaardscheidingsteken.

> [!TIP] In implementaties worden veel gebruikte scheidingstekens gevormd door een komma (`,`), een dubbele punt (`:`), een puntkomma (`;`) of een pipe (`|`). U kunt elk scheidingsteken gebruiken dat het beste bij uw implementatie past.

### Lijsteigenschappen instellen

Zodra u lijststeunen in de montages van de rapportreeks met het gewenste scheidingsteken vormt, zijn er geen implementatieverschillen behalve het gebruiken van het scheidingsteken.

```js
// List prop delimited with a comma
s.prop1 = "value1,value2,value3";
```

> [!IMPORTANT] Voor lijstprofielen geldt nog steeds de maximumlengte van 100 bytes. Lijstprofielen zijn eenvoudiger om deze limiet te bereiken en te worden afgekapt, omdat ze meerdere waarden kunnen bevatten. U kunt afkortingen of verkorte waarden gebruiken als deze limiet van 100 bytes wordt bereikt.
