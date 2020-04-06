---
title: eVar
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# eVar

*Deze Help-pagina beschrijft hoe eVars moet worden geïmplementeerd. Voor informatie over hoe eVars als afmeting werkt, zie[Vars](../../../components/c-variables/dimensionslist/reports-conversion.md)in de de gebruikersgids van Componenten.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken zoals u dat wilt.

>[!TIP] Adobe raadt u in de meeste gevallen aan eVars over props te gebruiken. In eerdere versies van Adobe Analytics hadden props en eVars voor- en nadelen voor elkaar. Adobe heeft echter verbeteringen aangebracht in Vars waarin vrijwel alle gevallen van gebruik voor props zijn opgenomen.

Zorg ervoor u registreert hoe u elk eVar en hun logica in uw document [van het](../../prepare/solution-design.md)oplossingsontwerp gebruikt.

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor u elke eVar in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

## Vars in Adobe Experience Platform Launch

U kunt eVars instellen tijdens het configureren van de extensie Analytics (globale variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel het [!UICONTROL Action Type] in op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL eVars] sectie.

U kunt een variabele selecteren om een waarde of gegevenselement in te stellen. U kunt de waarde ook uit een andere variabele Analytics kopiëren.

## s.eVar1 - s.eVar250 in AppMeasurement en Launch de redacteur van de douanecode

Elke eVar is een koord dat douanewaarden specifiek voor uw organisatie bevat. De maximale lengte is 255 bytes. Als waarden langer zijn dan 255 bytes, worden deze automatisch afgekapt wanneer ze naar Adobe worden verzonden.

```js
s.eVar1 = "Example custom value";
```

## Counter Vars

Var-waarden bevatten doorgaans een tekenreekswaarde. Nochtans, kunt u eVars vormen om in plaats daarvan een teller te bevatten. U wilt bijvoorbeeld het aantal interne zoekopdrachten tellen dat is uitgevoerd voordat u een aankoop doet. In plaats van een tekstwaarde in te stellen, gebruikt u de volgende syntaxis:

```js
// Increment a counter eVar by 1
s.eVar1 = "+1";

// Increment a counter eVar by 12.49
s.eVar1 = "+12.49";
```

Als er meer dan twee decimalen zijn opgegeven, wordt de teller afgerond tot twee decimalen. Een eVar teller kan geen negatieve aantallen bevatten.

>[!IMPORTANT] U moet eVars eerst configureren naar &#39;Counter&#39; in de beheerconsole voordat u tellervariabelen kunt gebruiken. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

## Exclusieve voordelen voor props of eVars

In de huidige versie van Adobe Analytics zijn props en eVars aangepaste variabelen met vergelijkbare mogelijkheden. Er zijn echter verschillende grote verschillen:

* De gegevens in steunen zijn beschikbaar in rapportering binnen notulen. eVars kunnen 30 minuten duren voordat ze in de rapportage worden weergegeven.
* Props hebben een limiet van 100 bytes in rapporten. Voor eVars geldt een limiet van 255 bytes.
* Props kunnen lijsteigenschappen worden, die meerdere waarden in dezelfde hit accepteren. Lijstvariabelen zijn een afzonderlijke variabele en er zijn slechts drie lijstvariabelen beschikbaar.
* Props blijven standaard behouden na de hit die ze hebben ingesteld. Vars hebben een aangepaste vervaldatum, zodat u kunt bepalen wanneer een eVar geen krediet meer krijgt voor een volgende gebeurtenis. Nochtans, als u de verwerking [van de](../../../components/vrs/vrs-report-time-processing.md)rapporttijd gebruikt, zowel kunnen de steunen als eVars een model van de douaneattributie gebruiken.
