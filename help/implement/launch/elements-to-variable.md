---
title: Gegevenselementen van start toewijzen aan analytische variabelen
description: Wijs gegevenselementen aan de variabelen van de Analyse toe zodat u hen als afmetingen in de Werkruimte van de Analyse kunt gebruiken.
translation-type: tm+mt
source-git-commit: 6937d47e3cf980a21bec680cdbd2931a4a368221

---


# Gegevenselementen van start toewijzen aan analytische variabelen

Als u een gegevensopslagruimte met gegevenselementen hebt in Adobe Experience Platform Launch, kunt u deze toewijzen aan Analytics-afmetingen.

## Vereisten

[Gegevenslaagobjecten toewijzen aan gegevenselementen](layer-to-elements.md): Zorg ervoor dat u gegevenselementen begrijpt in Lancering, en dat u verscheidene hebt om met te werken.

[Maak een document](../prepare/solution-design.md)voor het ontwerp van een oplossing: Een document van het oplossingsontwerp is essentieel om georganiseerd te blijven. Na uw document van het oplossingsontwerp vereenvoudigt de toewijzing van gegevenselementen aan variabelen van de Analyse.

## Gegevenselementen toewijzen aan analytische variabelen

Als u een bibliotheek in Launch publiceert nadat u deze stappen hebt uitgevoerd, kunt u aangepaste afmetingen gebruiken in de analysewerkruimte. U kunt variabelen van de Analyse globaal, of in individuele regels plaatsen.

### Algemene variabelen instellen

Algemene variabelen zijn ideaal als u variabelewaarden wilt instellen op alle pagina&#39;s waar het gegevenselement aanwezig is.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als daarom wordt gevraagd.
1. Klik op de gewenste eigenschap Launch.
1. Klik op de knop [!UICONTROL Extensions tab]en klik vervolgens [!UICONTROL Configure] onder de extensie Adobe Analytics.
1. Klik op de [!UICONTROL Global variables] accordeon, die de interface toont om globale variabelen toe te wijzen.

### Variabelen in regels instellen

Variabelen die in regels zijn ingesteld, zijn ideaal als u geen variabelen op elke pagina wilt instellen. U definieert de criteria in de regel. Zie de [regels](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/rules.html) in de gebruikershandleiding bij het Adobe Experience Platform Launch.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als daarom wordt gevraagd.
1. Klik op de gewenste eigenschap Launch.
1. Klik op het [!UICONTROL Rules] tabblad en klik vervolgens op de gewenste regel (of maak een regel).
1. Klik op de [!UICONTROL Add] knop onder [!UICONTROL Actions].
1. Stel het [!UICONTROL Extension] vervolgkeuzemenu in op Adobe Analytics en stel de optie Variabelen [!UICONTROL Action Type] in.
1. Klik op het pictogram van het element ![](assets/data-element.png) Gegevens rechts van de gewenste variabele Analytics. Het document [van het de](../prepare/solution-design.md) oplossingsontwerp van uw organisatie dicteert welke variabele Analytics aan gebruik.
1. Selecteer het gewenste gegevenselement in het modale venster. Klik op [!UICONTROL Select].
1. De naam van het gegevenselement wordt toegevoegd aan het tekstveld met `%` tekens. Als u bijvoorbeeld het gegevenselement &quot;Paginanaam&quot; een naam geeft, wordt de tekenreeks weergegeven `%Page name%` wanneer u een gegevenselement aan een variabele toewijst.

> [!TIP] U kunt gegevenselementen in dezelfde variabele samenvoegen. Als u bijvoorbeeld een gegevenselement &#39;Hostname&#39; en een gegevenselement &#39;Pathname&#39; hebt, kunt u beide elementen combineren in één variabele `%Hostname%%Pathname%`.

## Volgende stappen

[Paginariabelen](../vars/page-vars/page-variables.md): Leer welke variabelen op paginaniveau u in uw implementatie kunt gebruiken om meer uit dimensies in de Werkruimte van de Analyse te krijgen.

[Configuratievariabelen](../vars/config-vars/configuration-variables.md): Leer welke configuratievariabelen u in uw implementatie kunt gebruiken om meer eigenschappen in de Analytics van Adobe te ontgrendelen.
