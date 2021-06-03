---
title: Datalaagobjecten toewijzen aan data-elementen
description: Vorm Lancering om van uw gegevenslaag te lezen.
exl-id: b7594084-cb5f-408e-8a76-0a0815cc7553
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 6%

---

# Datalaagobjecten toewijzen aan data-elementen

Als uw organisatie een gegevenslaag op uw site heeft gemaakt en geïmplementeerd, kunt u gegevenslaagobjecten toewijzen aan gegevenselementen in Launch.

## Vereisten

[Een gegevenslaag](../prepare/data-layer.md) maken: Zorg ervoor dat er een gegevenslaag op uw site staat. Hoewel u technisch alle JavaScript-objecten kunt toewijzen of CSS-elementen rechtstreeks van de pagina kunt verwijderen, raadt Adobe deze praktijk aan als laatste redmiddel. Als de lay-out van uw site verandert, werken de CSS-kiezers die in Launch worden gebruikt niet meer, waardoor gegevens verloren gaan.

## Adobe Experience Platform Launch gebruiken om gegevenselementen te maken

[Gegevenselementen ](https://experienceleague.adobe.com/docs/launch/using/reference/manage-resources/data-elements.html#create-a-data-element) zijn componenten in Launch die u in het gereedschap kunt gebruiken. U kunt waarden van variabelen toewijzen in de Adobe Analytics-extensie met behulp van gegevenselementen.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
1. Klik op de gewenste eigenschap Launch.
1. Klik op de tab **[!UICONTROL Data Elements]** en klik vervolgens op **[!UICONTROL Add Data Element]**.

   ![gegevenselement maken](assets/createelement.png)

1. Voer een naam in voor het gegevenselement. Het kan een eenvoudig label zijn dat overeenkomt met een JavaScript-variabele in uw gegevenslaag die u wilt bijhouden.
1. Selecteer **[!UICONTROL Core]** onder het vervolgkeuzemenu **[!UICONTROL Extension]**.
1. Selecteer **[!UICONTROL JavaScript Variable]** onder het vervolgkeuzemenu **[!UICONTROL Data Element Type]**. Rechts wordt een tekstveld weergegeven waarin u de JavaScript-variabele kunt invoeren om aan dit gegevenselement toe te wijzen.
1. Voer de gewenste JavaScript-variabele in, meestal in de gegevenslaag. Als de gegevenslaag van uw organisatie bijvoorbeeld vrijwel overeenkomt met de aanbevolen Adobe, kan een waarde `digitalData.page.pageInfo.pageName` zijn. U kunt de browserconsole gebruiken om de syntaxis en waarden van JavaScript-variabelen te valideren.
1. Klik op **[!UICONTROL Save]**.

## Volgende stappen

[Gegevenselementen toewijzen aan analytische variabelen](elements-to-variable.md): Wijs gegevenselementen toe aan variabelen van de Analyse zodat u hen als afmetingen in Analysis Workspace kunt gebruiken.
