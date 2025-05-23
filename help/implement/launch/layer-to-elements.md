---
title: Gegevenslaagobjecten toewijzen aan gegevenselementen
description: Configureer codes die u van uw gegevenslaag wilt lezen.
feature: Tags
exl-id: b7594084-cb5f-408e-8a76-0a0815cc7553
role: Admin, Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 1%

---

# Gegevenslaagobjecten toewijzen aan gegevenselementen

Als uw organisatie een gegevenslaag op uw site heeft gemaakt en geïmplementeerd, kunt u gegevenslaagobjecten toewijzen aan gegevenselementen binnen tags.

## Vereisten

[Een gegevenslaag maken](../prepare/data-layer.md): Zorg ervoor dat er een gegevenslaag op uw site staat. Hoewel u technisch alle JavaScript-objecten kunt toewijzen of CSS-elementen rechtstreeks van de pagina kunt verwijderen, raadt de Adobe deze praktijk aan als laatste redmiddel. Als de lay-out van uw site verandert, werken de CSS-kiezers die in tags worden gebruikt niet meer, waardoor gegevens verloren gaan.

## Tags gebruiken om gegevenselementen te maken

[Gegevenselementen](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=nl-NL) Dit zijn componenten in Adobe Experience Platform Data Collection die u over het hulpmiddel kunt gebruiken. U kunt waarden van variabelen toewijzen in de Adobe Analytics-extensie met behulp van gegevenselementen.

1. Aanmelden bij [Adobe Experience Platform-gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Klik op de knop **[!UICONTROL Data Elements]** tab, en klik vervolgens op **[!UICONTROL Add Data Element]**.

   ![gegevenselement maken](assets/createelement.png)

1. Voer een naam in voor het gegevenselement. Het kan een eenvoudig label zijn dat overeenkomt met een JavaScript-variabele in uw gegevenslaag die u wilt bijhouden.
1. Onder de **[!UICONTROL Extension]** vervolgkeuzelijst, selecteert u **[!UICONTROL Core]**.
1. Onder de **[!UICONTROL Data Element Type]** vervolgkeuzelijst, selecteert u **[!UICONTROL JavaScript Variable]**. Rechts wordt een tekstveld weergegeven waarin u de JavaScript-variabele kunt invoeren om aan dit gegevenselement toe te wijzen.
1. Voer de gewenste JavaScript-variabele in, meestal in de gegevenslaag. Bijvoorbeeld, als de gegevenslaag van uw organisatie dicht de geadviseerde praktijk van de Adobe aanpast, kon een waarde zijn `digitalData.page.pageInfo.pageName`. Met de browserconsole kunt u de syntaxis en waarden van JavaScript-variabelen valideren.
1. Klik op **[!UICONTROL Save]**.

## Volgende stappen

[Gegevenselementen toewijzen aan analytische variabelen](elements-to-variable.md): Wijs gegevenselementen toe aan variabelen van de Analyse zodat u hen als afmetingen in Analysis Workspace kunt gebruiken.
