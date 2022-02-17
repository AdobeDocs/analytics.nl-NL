---
title: AppMeasurement gebruiken met iframes
description: Open Adobe Analytics-variabelen in een iframe of een bovenliggende pagina terwijl u zich in een iframe bevindt.
feature: Implementation Basics
exl-id: 59b9cd4f-8599-41ee-8b54-a6a556198ecd
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# AppMeasurement gebruiken met iframes

U kunt naar variabelen AppMeasurement van zowel kind als ouder iframes verwijzen. Het is noodzakelijk om alle variabelen in de zelfde plaats te bepalen waar de bibliotheek AppMeasurement bestaat. In de volgende voorbeelden wordt uitgelegd hoe u basisvariabelen en -methoden voor AppMeasurement binnen en buiten een iframe instelt.

Als u tags gebruikt in Adobe Experience Platform, moet u ervoor zorgen dat het tracker-object algemeen toegankelijk is. Zie [Overzicht Adobe Analytics-extensie](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/adobe/analytics/overview.html).

>[!CAUTION]
>
>Gebruik geen AppMeturement-bibliotheken op zowel een bovenliggende pagina als iframe. Dit brengt risico&#39;s met zich mee voor het verzenden van meerdere verzoeken om afbeeldingen, het opblazen van rapporten en het verhogen van aanroepbare serveraanroepen.

## Access AppMeasurement die zich in een iframe bevindt

U hebt toegang tot variabelen AppMeasurement via het iframe-object. Deze voorbeeldset [pageName](../vars/page-vars/pagename.md) en de [t(), methode](../vars/functions/t-method.md) twee verschillende manieren gebruiken om naar het iframe-object te verwijzen.

```js
// Reference AppMeasurement code that resides within an iframe and send an image request
document.getElementById('targetFrame').contentWindow.s.pageName="Page name within iframe";
document.getElementById('targetFrame').contentWindow.s.t();

// An alternate method to the above if there's only one iframe on the page
window.frames[0].contentWindow.s.pageName = "Page name within iframe";
window.frames[0].contentWindow.s.t();
```

## AppMeasurement openen vanuit een iframe

U hebt vanuit een iframe toegang tot variabelen van de klasse AppMeasurement op een bovenliggende pagina. Deze voorbeeldsets [pageName](../vars/page-vars/pagename.md) en roept de [t(), methode](../vars/functions/t-method.md) met de [`parent`](https://www.w3schools.com/jsref/prop_win_parent.asp) eigenschap.

```js
// Reference AppMeasurement code on a parent page from within an iframe and send an image request
parent.s.pageName = "Page Name on Hosted Window";
parent.s.t();
```

## Gebruiken `postMessage` en gebeurtenislisteners

U kunt ook `postMessage` en gebeurtenislisteners om variabelen in te stellen. Voor deze methode is geen directe verwijzing naar een iframe vereist.

```js
// Place this code in your parent window
function listenMessage(e) {
    if(e.data == "Example page view call") {
        s.pageName = "Page name using postMessage";
        s.t();
    }
}
window.addEventListener("message", listenMessage, false);

// Place this code in the iframe
window.top.postMessage("Example page view call","https://example.com");
```

## Beperkingen

* Net als bij andere JavaScript-code kunnen iframes alleen communiceren wanneer domeinen en protocol overeenkomen. Deze voorbeelden werken niet als de iframe-inhoud zich in een ander domein bevindt dan het bovenliggende domein.
* Als AppMeasurement zich in een iframe bevindt, [`referrer`](../vars/page-vars/referrer.md) De variabele wordt ingesteld op de bovenliggende URL, niet op de werkelijke verwijzende URL. U kunt de `referrer` variabele om dit probleem op te lossen.
* De [Adobe Experience Cloud debugger](https://experienceleague.adobe.com/docs/debugger/using/experience-cloud-debugger.html) worden afbeeldingsverzoeken die binnen iframes worden gestart, niet herkend.
* De Activity Map geeft de hitmap niet weer boven koppelingen die zijn geklikt binnen iframes. In plaats hiervan wordt het hele iframe gemarkeerd.
