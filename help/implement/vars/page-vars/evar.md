---
title: eVar
description: Aangepaste variabelen die u kunt gebruiken in uw implementatie.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 1%

---


# eVar

*Deze Help-pagina beschrijft hoe eVars moet worden geïmplementeerd. Voor informatie over hoe eVars als afmeting werkt, zie[Vars](/help/components/dimensions/evar.md)in de de gebruikersgids van Componenten.*

Variabelen zijn aangepaste variabelen die u kunt gebruiken zoals u dat wilt. Als u een document [van het](/help/implement/prepare/solution-design.md)oplossingsontwerp hebt, komen de meeste dimensies specifiek voor uw organisatie tot eVars. Standaard blijven de eVars behouden na de hit waarop ze zijn ingesteld. U kunt hun vervaldatum en toewijzing onder de variabelen [van de](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) Omzetting in de montages van de Reeks van het Rapport aanpassen.

Het aantal beschikbare eVars is afhankelijk van uw contract met Adobe. Er zijn maximaal 250 eVars beschikbaar als uw contract met Adobe dit ondersteunt.

## Vars instellen in instellingen van rapportsuite

Alvorens eVars in uw implementatie te gebruiken, zorg ervoor u elke eVar in de montages van de rapportreeks vormt. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.

## Vars in Adobe Experience Platform Launch

U kunt eVars instellen tijdens het configureren van de Analytics-extensie (globale variabelen) of onder regels.

1. Meld u aan bij [launch.adobe.com](https://launch.adobe.com) met uw Adobe-id-referenties.
2. Klik op de gewenste eigenschap.
3. Ga naar het [!UICONTROL Rules] lusje, dan klik de gewenste regel (of creeer een regel).
4. Klik onder [!UICONTROL Actions]op een bestaande [!UICONTROL Adobe Analytics - Set Variables] handeling of klik op het pictogram ‘+’.
5. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en [!UICONTROL Action Type] op [!UICONTROL Set Variables].
6. Zoek de [!UICONTROL eVars] sectie.

U kunt een eVar aan een waarde of een gegevenselement plaatsen. U kunt de waarde ook uit een andere Analytics-variabele kopiëren.

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

>[!IMPORTANT]
>
>U moet eVars aan &quot;Teller&quot;in de Admin Console eerst vormen alvorens tellervariabelen te gebruiken. Zie [Conversievariabelen](/help/admin/admin/conversion-var-admin/conversion-var-admin.md) in de handleiding Admin.
