---
title: Taggegevenselementen toewijzen aan analytische variabelen
description: Wijs gegevenselementen toe aan variabelen van de Analyse zodat u hen als afmetingen in Analysis Workspace kunt gebruiken.
feature: Launch Implementation
exl-id: 996c1204-3f8a-453e-8104-5e8e1279517c
source-git-commit: f4b495b11bcbd55bc8448f2c9c09268547fb9750
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# Taggegevenselementen toewijzen aan analytische variabelen

Als u een opslagplaats hebt met taggegevenselementen, kunt u deze toewijzen aan Analytics-afmetingen.

## Vereisten

[Gegevenslaagobjecten toewijzen aan gegevenselementen](layer-to-elements.md): Zorg ervoor dat u de elementen van de markeringsgegevens begrijpt, en dat u verscheidene hebt om met te werken.

[Een document voor het ontwerp van een oplossing maken](../prepare/solution-design.md): Een document van het oplossingsontwerp is essentieel om georganiseerd te blijven. Na uw document van het oplossingsontwerp vereenvoudigt de toewijzing van gegevenselementen aan variabelen van de Analyse.

## Gegevenselementen toewijzen aan analytische variabelen

Als u een tagbibliotheek publiceert nadat u deze stappen hebt uitgevoerd, kunt u aangepaste afmetingen gebruiken in Analysis Workspace. U kunt variabelen van de Analyse globaal, of in individuele regels plaatsen.

### Algemene variabelen instellen

Algemene variabelen zijn ideaal als u variabelewaarden wilt instellen op alle pagina&#39;s waar het gegevenselement aanwezig is.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Klik op de knop [!UICONTROL Extensions tab]en klik vervolgens op [!UICONTROL Configure] onder de extensie Adobe Analytics.
1. Klik op de knop [!UICONTROL Global variables] accordion, die de interface onthult om globale variabelen toe te wijzen.

### Variabelen in regels instellen

Variabelen die in regels zijn ingesteld, zijn ideaal als u geen variabelen op elke pagina wilt instellen. U definieert de criteria in de regel. Zie [Regels](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/rules.html) in de Adobe Experience Platform-tagdocumentatie.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Klik op de knop [!UICONTROL Rules] klikt u op de gewenste regel (of maakt u een regel).
1. Klik op de knop [!UICONTROL Add] knop onder [!UICONTROL Actions].
1. Stel de [!UICONTROL Extension] en de [!UICONTROL Action Type] om variabelen in te stellen.
1. Klik op de knop ![Gegevenselement](assets/data-element.png) rechts van de gewenste variabele Analytics. De [document ontwerp oplossing](../prepare/solution-design.md) Hiermee bepaalt u welke variabele Analytics moet worden gebruikt.
1. Selecteer het gewenste gegevenselement in het modale venster. Klik op [!UICONTROL Select].
1. De naam van het gegevenselement wordt toegevoegd aan het tekstveld dat wordt omgeven door `%` tekens. Als u bijvoorbeeld het gegevenselement &quot;Paginanaam&quot; een naam geeft, wordt de tekenreeks weergegeven `%Page name%` bij het toewijzen van een gegevenselement aan een variabele.

>[!TIP]
>
>U kunt gegevenselementen in dezelfde variabele samenvoegen. Als u bijvoorbeeld een gegevenselement &#39;Hostname&#39; en een gegevenselement &#39;Pathname&#39; hebt, kunt u beide elementen combineren in één variabele met `%Hostname%%Pathname%`.

## Volgende stappen

[Paginariabelen](../vars/page-vars/page-variables.md): Leer welke variabelen op paginaniveau u in uw implementatie kunt gebruiken om meer uit afmetingen in Analysis Workspace te krijgen.

[Configuratievariabelen](../vars/config-vars/configuration-variables.md): Leer welke configuratievariabelen u in uw implementatie kunt gebruiken om meer eigenschappen in Adobe Analytics te ontgrendelen.
