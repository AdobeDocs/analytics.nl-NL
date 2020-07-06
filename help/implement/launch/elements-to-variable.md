---
title: Launch-data-elementen Analytics-variabelen
description: Wijs gegevenselementen toe aan Analytics-variabelen zodat u deze als afmetingen kunt gebruiken in Analysis Workspace.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '436'
ht-degree: 7%

---


# Launch-data-elementen Analytics-variabelen

Zodra u een bewaarplaats van gegevenselementen in de Lancering van het Adobe Experience Platform hebt, kunt u hen aan de dimensies van Analytics toewijzen.

## Vereisten

[Gegevenslaagobjecten toewijzen aan gegevenselementen](layer-to-elements.md): Zorg ervoor dat u gegevenselementen begrijpt in Lancering, en dat u verscheidene hebt om met te werken.

[Maak een document](../prepare/solution-design.md)voor het ontwerp van een oplossing: Een document van het oplossingsontwerp is essentieel om georganiseerd te blijven. Na uw document van het oplossingsontwerp vereenvoudigt de toewijzing van gegevenselementen aan de variabelen van Analytics.

## Gegevenselementen toewijzen aan Analytics-variabelen

Als u een bibliotheek in Launch publiceert nadat u deze stappen hebt uitgevoerd, kunt u aangepaste afmetingen gebruiken in Analysis Workspace. U kunt Analytics-variabelen globaal of volgens afzonderlijke regels instellen.

### Algemene variabelen instellen

Algemene variabelen zijn ideaal als u variabelewaarden wilt instellen op alle pagina&#39;s waar het gegevenselement aanwezig is.

1. Ga naar [Adobe Experience Platform starten](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de gewenste eigenschap Launch.
1. Klik op de extensie [!UICONTROL Extensions tab]en klik vervolgens [!UICONTROL Configure] onder de extensie Adobe Analytics.
1. Klik op de [!UICONTROL Global variables] accordeon, die de interface toont om globale variabelen toe te wijzen.

### Variabelen in regels instellen

Variabelen die in regels zijn ingesteld, zijn ideaal als u geen variabelen op elke pagina wilt instellen. U definieert de criteria in de regel. Zie [Regels](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/rules.html) in de de gebruikersgids van de Lancering van het Adobe Experience Platform.

1. Ga naar [Adobe Experience Platform starten](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de gewenste eigenschap Launch.
1. Klik op het [!UICONTROL Rules] tabblad en klik vervolgens op de gewenste regel (of maak een regel).
1. Click the [!UICONTROL Add] button under [!UICONTROL Actions].
1. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel de optie Variabelen [!UICONTROL Action Type] in.
1. Klik op het pictogram ![Gegevenselement](assets/data-element.png) rechts van de gewenste Analytics-variabele. Het document [van het de](../prepare/solution-design.md) oplossingsontwerp van uw organisatie dicteert welke variabele van Analytics te gebruiken.
1. Selecteer het gewenste gegevenselement in het modale venster. Klik op [!UICONTROL Select].
1. De naam van het gegevenselement wordt toegevoegd aan het tekstveld met `%` tekens. Als u bijvoorbeeld het gegevenselement &quot;Paginanaam&quot; een naam geeft, wordt de tekenreeks weergegeven `%Page name%` wanneer u een gegevenselement aan een variabele toewijst.

>[!TIP]
>
>U kunt gegevenselementen in dezelfde variabele samenvoegen. Als u bijvoorbeeld een gegevenselement &#39;Hostname&#39; en een gegevenselement &#39;Pathname&#39; hebt, kunt u beide elementen combineren in één variabele `%Hostname%%Pathname%`.

## Volgende stappen

[Paginariabelen](../vars/page-vars/page-variables.md): Leer welke variabelen op paginaniveau u in uw implementatie kunt gebruiken om meer uit afmetingen in Analysis Workspace te krijgen.

[Configuratievariabelen](../vars/config-vars/configuration-variables.md): Leer welke configuratievariabelen u in uw implementatie kunt gebruiken om meer eigenschappen in Adobe Analytics te ontgrendelen.
