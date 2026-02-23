---
title: Overzicht van variabelen, functies, methoden en plug-ins
description: Leer welke variabelen u kunt opnemen in de gegevens die u naar Adobe verzendt om de rapportage te verbeteren.
keywords: toepassingsmeting,variabelen,vars,configuratie,pagina,implementatie
feature: Appmeasurement Implementation
exl-id: 7ffcd943-f9ac-4daf-bbdf-248d75925b04
role: Admin, Developer
source-git-commit: 8b1e25b9633b6db3e49da079f7014e6b7b595474
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# Overzicht van variabelen, functies, methoden en plug-ins

Analytics biedt een aantal variabelen voor het verzamelen van analysegegevens. Variabelen in deze sectie worden in verschillende secties gesplitst:

* **variabelen van de Pagina** zijn waarden die typisch direct in het melden worden gebruikt. Veelvoorkomende paginariabelen zijn `props` , `eVars` en `events` .
* **Config variabelen** zijn montagewaarden die helpen ervoor zorgen de correcte gegevens Adobe bereikt. Veelvoorkomende configuratievariabelen zijn `trackingServerSecure` , `charSet` en `linkTrackVars` . In configuratievariabelen worden dimensie-items gewoonlijk niet gevuld.
* **Functies en methodes** zijn stukken van code die een specifieke taak wanneer van verwijzingen voorzien uitvoeren. Veelvoorkomende functies zijn `t()` , `tl()` en `clearVars()` .

## Variabelen en implementatiemethoden

Adobe biedt meerdere manieren om Adobe Analytics te implementeren. Elke pagina biedt een sectie op aan hoe te om de variabele uit te voeren gebruikend het Web SDK, gebruikend de uitbreiding van Adobe Analytics, en gebruikend AppMeasurement voor JavaScript.


>[!BEGINSHADEBOX]

Zie ![&#x200B; VideoCheckedOut &#x200B;](/help/assets/icons/VideoCheckedOut.svg) [&#x200B; Vormende variabelen &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-learn/tutorials/administration/manage-report-suites/configuring-variables-in-the-admin-console){target="_blank"} voor een demo video.

>[!ENDSHADEBOX]


## Volgorde van de verrichtingen

AppMeasurement-bibliotheken die door Adobe Analytics worden gepubliceerd, hebben een specifieke volgorde bij het verzenden van gegevens naar Adobe. Als u deze taken uit orde uitvoert, kunnen de gegevens onvolledig zijn.

1. Als uw site een gegevenslaag gebruikt, moet u ervoor zorgen dat eerst alle toepasselijke variabelen worden ingevuld. U vult `adobeDataLayer.page.title` bijvoorbeeld met de paginatitel. Zie [&#x200B; de laag van Gegevens &#x200B;](../prepare/data-layer.md) voor meer informatie.
2. Gebruik de gegevenslaag om analytische variabelen te vullen. <br/> als u markeringen in Adobe Experience Platform gebruikt, wordt deze taak verwezenlijkt door gegevenselementen binnen tussen te gebruiken. Gegevenselementen worden gevuld met waarden uit de gegevenslaag. Het gegevenselement `Page Title` haalt bijvoorbeeld de waarde op uit de variabele van de gegevenslaag `adobeDataLayer.page.title` . <br/> dan kunt u het gegevenselement gebruiken om de variabelen van de Analyse te bevolken. `eVar4` haalt bijvoorbeeld de waarde op uit het gegevenselement `Page Title` . <br/> zie voor meer informatie [&#x200B; de elementen van Gegevens &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/data-elements.html), [&#x200B; de voorwerpen van de de gegevenslaag van de Kaart aan gegevenselementen &#x200B;](../launch/layer-to-elements.md), en [&#x200B; de elementen van de markeringsgegevens van de Kaart aan de variabelen van de Analyse &#x200B;](../launch/elements-to-variable.md)
3. Tot slot roep de functie tracking. De meeste AppMeasurement-bibliotheken gebruiken de methode `t()` , maar sommige mobiele SDK gebruiken `track()` . Wanneer de functie tracking wordt aangeroepen, worden alle ondersteunde variabelen die in het object Analytics zijn gedefinieerd, naar Adobe verzonden in de vorm van een afbeeldingsaanvraag.

## Ongeldige tekens

De volgende tekens en tekenreeksen zijn nooit toegestaan in JavaScript-variabelen.

* Tab (`0x09`)
* Enter (`0x0D`)
* Newline (`0x0A`)
* HTML-tags (bijvoorbeeld `<b></b>` of `&#153` )

Sommige variabelen hebben extra beperkingen of syntaxisvereisten. Met de variabele [`products`](page-vars/products.md) worden bijvoorbeeld puntkomma&#39;s en komma&#39;s gereserveerd om afzonderlijke producten en categorieën te scheiden.
