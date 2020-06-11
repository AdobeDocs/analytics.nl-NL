---
title: prop
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
translation-type: tm+mt
source-git-commit: 10e157e370367374b55ee9c87c0e5c7ca9e99c1a
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---


# prop

*Deze Help-pagina beschrijft hoe u instructies kunt implementeren. Voor informatie over hoe de steunen als afmeting werken, zie[steun](/help/components/dimensions/prop.md)in de de gebruikersgids van Componenten.*

Props zijn aangepaste variabelen die u op de gewenste manier kunt gebruiken. Ze blijven niet bestaan na de hit die ze zijn ingesteld.

> [!TIP] Adobe raadt u in de meeste gevallen aan [eVars](evar.md) te gebruiken. In eerdere versies van Adobe Analytics hadden props en eVars voor- en nadelen voor elkaar. Adobe heeft echter verbeteringen aangebracht in Vars waarin vrijwel alle gevallen van gebruik voor props zijn opgenomen.

Als u een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp hebt, kunt u deze douanedimensies aan waarden toewijzen specifiek voor uw organisatie. Het aantal beschikbare proefdrukken is afhankelijk van uw contract met Adobe. Er zijn maximaal 75 props beschikbaar als uw contract met Adobe dit ondersteunt.

## Props in Adobe Experience Platform Launch

U kunt eigenschappen instellen tijdens het configureren van de extensie Analytics (algemene variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL Props] sectie.

U kunt een eigenschap instellen op een waarde of een gegevenselement. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

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

Als u dezelfde waarde meerdere keren instelt in een lijst-eigenschap, wordt de duplicatie ongedaan gemaakt in de rapportage. De Werkruimte van de Analyse telt het aantal treffers waar een waarde wordt gezien, en niet het aantal tijden een waarde in gegevens bestaat.
