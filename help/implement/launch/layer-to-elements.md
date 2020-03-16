---
title: Gegevenslaagobjecten toewijzen aan gegevenselementen
description: Vorm Lancering om van uw gegevenslaag te lezen.
translation-type: tm+mt
source-git-commit: 283fcd5832abe4c09caa332c2ebc3a22029e6707

---


# Gegevenslaagobjecten toewijzen aan gegevenselementen

Als uw organisatie een gegevenslaag op uw site heeft gemaakt en geïmplementeerd, kunt u gegevenslaagobjecten toewijzen aan gegevenselementen in Launch.

## Vereisten

[Een gegevenslaag](../prepare/data-layer.md)maken: Zorg ervoor dat er een gegevenslaag op uw site staat. Hoewel u technisch alle JavaScript-objecten kunt toewijzen of CSS-elementen rechtstreeks van de pagina kunt verwijderen, raadt Adobe deze praktijk aan als laatste redmiddel. Als de lay-out van uw site verandert, werken de CSS-kiezers die in Launch worden gebruikt niet meer, waardoor gegevens verloren gaan.

## Adobe Experience Platform Launch gebruiken om gegevenselementen te maken

[Gegevenselementen](https://docs.adobe.com/content/help/en/launch/using/reference/manage-resources/data-elements.html#create-a-data-element) zijn componenten in Launch die u in het gereedschap kunt gebruiken. U kunt met behulp van gegevenselementen variabelewaarden toewijzen in de extensie Adobe Analytics.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als daarom wordt gevraagd.
1. Klik op de gewenste eigenschap Launch.
1. Klik op het [!UICONTROL Data Elements] tabblad en klik vervolgens op [!UICONTROL Add Data Element].

   ![gegevenselement maken](assets/createelement.png)

1. Voer een naam in voor het gegevenselement. Het kan een eenvoudig label zijn dat overeenkomt met een JavaScript-variabele in uw gegevenslaag die u wilt bijhouden.
1. Selecteer onder het [!UICONTROL Extension] vervolgkeuzemenu [!UICONTROL Core].
1. Selecteer onder het [!UICONTROL Data Element Type] vervolgkeuzemenu [!UICONTROL JavaScript Variable]. Rechts wordt een tekstveld weergegeven waarin u de JavaScript-variabele kunt invoeren om aan dit gegevenselement toe te wijzen.
1. Voer de gewenste JavaScript-variabele in, meestal in de gegevenslaag. Als de gegevenslaag van uw organisatie bijvoorbeeld vrijwel overeenkomt met de aanbevolen werkwijze van Adobe, kan een waarde worden opgegeven. `digitalData.page.pageInfo.pageName` U kunt de browserconsole gebruiken om de syntaxis en waarden van JavaScript-variabelen te valideren.
1. Klik op [!UICONTROL Save].

## Volgende stappen

[Gegevenselementen toewijzen aan analytische variabelen](elements-to-variable.md): Wijs gegevenselementen aan de variabelen van de Analyse toe zodat u hen als afmetingen in de Werkruimte van de Analyse kunt gebruiken.
