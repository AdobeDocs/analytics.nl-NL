---
title: Overzicht van variabelen, functies, methoden en plug-ins
description: Leer welke variabelen u in de gegevens kunt omvatten u naar Adobe verzendt om rapportering te verbeteren.
keywords: toepassingsmeting,variabelen,vars,configuratie,pagina,implementatie
feature: Variables
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
source-git-commit: 1516a1353c1b0a3b7365c3e3f10ce74ae1255696
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 0%

---

# Overzicht van variabelen, functies, methoden en plug-ins

Analytics biedt een aantal variabelen voor het verzamelen van analysegegevens. Variabelen in deze sectie worden in verschillende secties gesplitst:

* **Paginariabelen** zijn waarden die doorgaans rechtstreeks bij de rapportage worden gebruikt. Veelvoorkomende paginavariabelen zijn `props`, `eVars`, en `events`.
* **Config-variabelen** Dit zijn instellingenwaarden die ervoor zorgen dat de juiste gegevens Adobe bereiken. Veelvoorkomende configuratievariabelen zijn `trackingServerSecure`, `charSet`, en `linkTrackVars`. In configuratievariabelen worden dimensie-items gewoonlijk niet gevuld.
* **Functies en methoden** zijn stukken code die een specifieke taak uitvoeren wanneer van verwijzingen wordt voorzien. Veelvoorkomende functies zijn `t()`, `tl()`, en `clearVars()`.

## Variabelen en uitvoeringsmethoden

Adobe biedt meerdere manieren om Adobe Analytics te implementeren. Elke pagina biedt een sectie over hoe te om de variabele uit te voeren gebruikend het Web SDK, gebruikend de uitbreiding van Adobe Analytics, en gebruikend AppMeasurement voor JavaScript.

Hier volgt een video over het configureren van variabelen in Adobe Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/28755/?quality=12)

## Volgorde van de verrichtingen

De bibliotheken van het AppMeasurement die door Adobe Analytics worden gepubliceerd volgen een specifieke orde wanneer het verzenden van gegevens naar Adobe. Als u deze taken uit orde uitvoert, kunnen de gegevens onvolledig zijn.

1. Als uw site een gegevenslaag gebruikt, moet u ervoor zorgen dat eerst alle toepasselijke variabelen worden ingevuld. U vult bijvoorbeeld `adobeDataLayer.page.title` met de paginatitel. Zie [Gegevenslaag](../prepare/data-layer.md) voor meer informatie .
2. Gebruik de gegevenslaag om analytische variabelen te vullen. <br/>Als u tags gebruikt in Adobe Experience Platform, wordt deze taak uitgevoerd met behulp van gegevenselementen ertussen. Gegevenselementen worden gevuld met waarden uit de gegevenslaag. Bijvoorbeeld gegevenselement `Page Title` Hiermee wordt de waarde opgehaald uit de variabele van de gegevenslaag `adobeDataLayer.page.title`. <br/>Vervolgens kunt u het gegevenselement gebruiken om analytische variabelen te vullen. Bijvoorbeeld `eVar4` Hiermee wordt de waarde opgehaald uit het gegevenselement `Page Title`. <br/>Zie voor meer informatie [Gegevenselementen](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html), [Gegevenslaagobjecten toewijzen aan gegevenselementen](../launch/layer-to-elements.md), en [Taggegevenselementen toewijzen aan analytische variabelen](../launch/elements-to-variable.md)
3. Tot slot roep de functie tracking. De meeste bibliotheken met AppMeasurementen gebruiken de `t()` echter, sommige mobiele SDK&#39;s gebruiken `track()`. Wanneer de functie tracking wordt aangeroepen, worden alle ondersteunde variabelen die in het object Analytics zijn gedefinieerd, naar Adobe verzonden in de vorm van een afbeeldingsaanvraag.

## Ongeldige tekens

De volgende tekens en tekenreeksen zijn nooit toegestaan in JavaScript-variabelen.

* Tab (`0x09`)
* Regeleinde (`0x0D`)
* Newline (`0x0A`)
* HTML-tags (bijvoorbeeld `<b></b>` of `&#153`)

Sommige variabelen hebben extra beperkingen of syntaxisvereisten. De [`products`](page-vars/products.md) met variabele reserves worden puntkomma &#39; s en komma &#39; s als scheidingsprodukten en categorieën aangemerkt .
