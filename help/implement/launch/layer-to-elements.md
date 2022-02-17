---
title: Datalaagobjecten toewijzen aan data-elementen
description: Configureer codes die u van uw gegevenslaag wilt lezen.
feature: Launch Implementation
exl-id: b7594084-cb5f-408e-8a76-0a0815cc7553
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 5%

---

# Datalaagobjecten toewijzen aan data-elementen

Als uw organisatie een gegevenslaag op uw site heeft gemaakt en geïmplementeerd, kunt u gegevenslaagobjecten toewijzen aan gegevenselementen binnen tags.

>[!NOTE]
>Adobe Experience Platform Launch is omgedoopt tot een reeks technologieën voor gegevensverzameling in Experience Platform. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

## Vereisten

[Een gegevenslaag maken](../prepare/data-layer.md): Zorg ervoor dat er een gegevenslaag op uw site staat. Hoewel u technisch alle JavaScript-objecten kunt toewijzen of CSS-elementen rechtstreeks van de pagina kunt verwijderen, raadt Adobe deze praktijk aan als laatste redmiddel. Als de lay-out van uw site verandert, werken de CSS-kiezers die in tags worden gebruikt niet meer, waardoor gegevens verloren gaan.

## Tags gebruiken om gegevenselementen te maken

[Gegevenselementen](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html?lang=en) zijn componenten in de UI van de Inzameling van Gegevens die u over het hulpmiddel kunt gebruiken. U kunt waarden van variabelen toewijzen in de Adobe Analytics-extensie met behulp van gegevenselementen.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
1. Klik op de gewenste tageigenschap.
1. Klik op de knop **[!UICONTROL Data Elements]** tab, en klik vervolgens op **[!UICONTROL Add Data Element]**.

   ![gegevenselement maken](assets/createelement.png)

1. Voer een naam in voor het gegevenselement. Het kan een eenvoudig label zijn dat overeenkomt met een JavaScript-variabele in uw gegevenslaag die u wilt bijhouden.
1. Onder de **[!UICONTROL Extension]** vervolgkeuzelijst, selecteren **[!UICONTROL Core]**.
1. Onder de **[!UICONTROL Data Element Type]** vervolgkeuzelijst, selecteren **[!UICONTROL JavaScript Variable]**. Rechts wordt een tekstveld weergegeven waarin u de JavaScript-variabele kunt invoeren om aan dit gegevenselement toe te wijzen.
1. Voer de gewenste JavaScript-variabele in, meestal in de gegevenslaag. Als de gegevenslaag van uw organisatie bijvoorbeeld vrijwel overeenkomt met de aanbevolen Adobe, kan een waarde `digitalData.page.pageInfo.pageName`. U kunt de browserconsole gebruiken om de syntaxis en waarden van JavaScript-variabelen te valideren.
1. Klik op **[!UICONTROL Save]**.

## Volgende stappen

[Gegevenselementen toewijzen aan analytische variabelen](elements-to-variable.md): Wijs gegevenselementen toe aan variabelen van de Analyse zodat u hen als afmetingen in Analysis Workspace kunt gebruiken.
