---
title: Overzicht van variabelen, functies, methoden en plug-ins
description: Leer welke variabelen u in de gegevens kunt omvatten u naar Adobe verzendt om rapportering te verbeteren.
keywords: toepassingsmeting,variabelen,vars,configuratie,pagina,implementatie
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
source-git-commit: f52623f4885063d080c95ef275808a3d051895e5
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---

# Overzicht van variabelen, functies, methoden en plug-ins

Analytics biedt een aantal variabelen voor het verzamelen van analysegegevens. Variabelen in deze sectie worden in verschillende secties gesplitst:

* **Paginabariabelen** zijn waarden die doorgaans rechtstreeks worden gebruikt voor rapportage. Veelvoorkomende paginariabelen zijn `props`, `eVars` en `events`.
* **Config-** variabelen zijn instellingswaarden die ervoor zorgen dat de juiste gegevens de Adobe bereiken. Veelvoorkomende configuratievariabelen zijn `trackingServerSecure`, `charSet` en `linkTrackVars`. In configuratievariabelen worden dimensie-items gewoonlijk niet gevuld.
* **Functies en** methoden zijn stukken code die een specifieke taak uitvoeren wanneer ernaar wordt verwezen. Veelvoorkomende functies zijn `t()`, `tl()` en `clearVars()`.

## Variabelen en uitvoeringsmethoden

Adobe biedt meerdere manieren om Adobe Analytics te implementeren. Elke pagina bevat een sectie over het implementeren van de variabele met behulp van tags in Adobe Experience Platform en AppMeasurement voor JavaScript.

Hier volgt een video over het configureren van variabelen in Adobe Analytics:

>[!VIDEO](https://video.tv.adobe.com/v/28755/?quality=12)

## Volgorde van de verrichtingen

AppMeasurement-bibliotheken die door Adobe Analytics worden gepubliceerd, hebben een specifieke volgorde bij het verzenden van gegevens naar Adobe. Als u deze taken uit orde uitvoert, kunnen de gegevens onvolledig zijn.

1. Als uw site een gegevenslaag gebruikt, moet u ervoor zorgen dat eerst alle toepasselijke variabelen worden ingevuld. Zie [Gegevenslaag](../prepare/data-layer.md) voor meer informatie.
2. Gebruik de gegevenslaag om analytische variabelen te vullen. Als u tags gebruikt in Adobe Experience Platform, kunt u deze taak eenvoudig uitvoeren met behulp van gegevenselementen en vervolgens het gegevenselement toewijzen aan een variabele. Zie [Gegevenselementen](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html).
3. Roep de functie tracking aan. De meeste AppMeasurement-bibliotheken gebruiken de methode `t()`, maar sommige mobiele SDK&#39;s gebruiken `track()`. Wanneer de functie tracking wordt aangeroepen, worden alle ondersteunde variabelen die in het object Analytics zijn gedefinieerd, naar Adobe verzonden in de vorm van een afbeeldingsaanvraag.

## Ongeldige tekens

De volgende tekens en tekenreeksen zijn nooit toegestaan in JavaScript-variabelen.

* Tab (`0x09`)
* Regeleinde (`0x0D`)
* Newline (`0x0A`)
* HTML-tags (bijvoorbeeld `<b></b>` of `&#153`)

Sommige variabelen hebben extra beperkingen of syntaxisvereisten. Met de variabele [`products`](page-vars/products.md) worden bijvoorbeeld puntkomma&#39;s en komma&#39;s gereserveerd om afzonderlijke producten en categorieën te scheiden.
