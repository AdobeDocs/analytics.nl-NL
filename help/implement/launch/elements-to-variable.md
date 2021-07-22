---
title: Taggegevenselementen toewijzen aan analytische variabelen
description: Wijs gegevenselementen toe aan variabelen van de Analyse zodat u hen als afmetingen in Analysis Workspace kunt gebruiken.
exl-id: 996c1204-3f8a-453e-8104-5e8e1279517c
source-git-commit: 5368e808a862a3e320f5d079433db96ab79b45c8
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 1%

---

# Taggegevenselementen toewijzen aan analytische variabelen

Als u een opslagplaats hebt met taggegevenselementen, kunt u deze toewijzen aan Analytics-afmetingen.

>[!NOTE]
>Adobe Experience Platform Launch is omgedoopt tot een reeks technologieën voor gegevensverzameling in Experience Platform. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

## Vereisten

[Gegevenslaagobjecten toewijzen aan gegevenselementen](layer-to-elements.md): Zorg ervoor dat u de elementen van de markeringsgegevens begrijpt, en dat u verscheidene hebt om met te werken.

[Maak een document](../prepare/solution-design.md) voor het ontwerp van een oplossing: Een document van het oplossingsontwerp is essentieel om georganiseerd te blijven. Na uw document van het oplossingsontwerp vereenvoudigt de toewijzing van gegevenselementen aan variabelen van de Analyse.

## Gegevenselementen toewijzen aan analytische variabelen

Als u een tagbibliotheek publiceert nadat u deze stappen hebt uitgevoerd, kunt u aangepaste afmetingen gebruiken in Analysis Workspace. U kunt variabelen van de Analyse globaal, of in individuele regels plaatsen.

### Algemene variabelen instellen

Algemene variabelen zijn ideaal als u variabelewaarden wilt instellen op alle pagina&#39;s waar het gegevenselement aanwezig is.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de gewenste tageigenschap.
1. Klik op [!UICONTROL Extensions tab] en klik vervolgens onder de extensie Adobe Analytics op [!UICONTROL Configure].
1. Klik op de accordion [!UICONTROL Global variables], die de interface onthult om globale variabelen toe te wijzen.

### Variabelen in regels instellen

Variabelen die in regels zijn ingesteld, zijn ideaal als u geen variabelen op elke pagina wilt instellen. U definieert de criteria in de regel. Zie [Regels](https://experienceleague.adobe.com/docs/launch/using/reference/manage-resources/rules.html) in de Adobe Experience Platform Launch-gebruikershandleiding.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de gewenste tageigenschap.
1. Klik op het tabblad [!UICONTROL Rules] en klik vervolgens op de gewenste regel (of maak er een).
1. Klik op de knop [!UICONTROL Add] onder [!UICONTROL Actions].
1. Stel het vervolgkeuzemenu [!UICONTROL Extension] in op Adobe Analytics en [!UICONTROL Action Type] op Variabelen instellen.
1. Klik op het pictogram ![Gegevenselement](assets/data-element.png) rechts van de gewenste variabele Analytics. Het [document van het oplossingsontwerp ](../prepare/solution-design.md) van uw organisatie bepaalt welke variabele Analytics aan gebruik.
1. Selecteer het gewenste gegevenselement in het modale venster. Klik op [!UICONTROL Select].
1. De naam van het gegevenselement wordt toegevoegd aan het tekstveld dat wordt omringd door `%` tekens. Als u bijvoorbeeld het gegevenselement &quot;Paginanaam&quot; een naam geeft, ziet u de tekenreeks `%Page name%` wanneer u een gegevenselement toewijst aan een variabele.

>[!TIP]
>
>U kunt gegevenselementen in dezelfde variabele samenvoegen. Als u bijvoorbeeld een gegevenselement &#39;Hostname&#39; en een gegevenselement &#39;Pathname&#39; hebt, kunt u beide elementen combineren in één variabele met `%Hostname%%Pathname%`.

## Volgende stappen

[Paginariabelen](../vars/page-vars/page-variables.md): Leer welke variabelen op paginaniveau u in uw implementatie kunt gebruiken om meer uit afmetingen in Analysis Workspace te krijgen.

[Configuratievariabelen](../vars/config-vars/configuration-variables.md): Leer welke configuratievariabelen u in uw implementatie kunt gebruiken om meer eigenschappen in Adobe Analytics te ontgrendelen.
