---
title: Implementeren met AJAX
description: Leer hoe u Adobe Analytics op een site implementeert met AJAX.
feature: Implementation Basics
exl-id: 3286bf97-3a66-4f68-9053-bf84269962fd
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 0%

---

# Implementeren met AJAX

AJAX is een praktijk waarbij u JavaScript en HTML gebruikt om inhoud te wissen en te genereren zonder een nieuwe pagina te laden.

Adobe Analytics is gewoonlijk afhankelijk van pagina&#39;s die opnieuw worden geladen om het object Analytics tracking opnieuw in te stellen. Telkens wanneer u naar een andere URL navigeert, worden alle variabelen van de Analyse opnieuw ingesteld en kunnen deze opnieuw worden gedefinieerd. Wanneer u AJAX op uw site gebruikt, past u de implementatie aan bij het ontbreken van pagina-vernieuwingen om ervoor te zorgen dat gegevens niet onjuist blijven bestaan tussen treffers.

Als u maatregelen hebt ingesteld om variabele waarden te wissen, is het implementeren van Adobe Analytics op sites die AJAX gebruiken meestal hetzelfde als andere implementatiemethoden.

## Interacties en raaktypen bepalen

Aangezien pagina&#39;s die AJAX gebruiken doorgaans niet opnieuw worden geladen, kan een gebruiker meerdere interacties op uw site uitvoeren. Wanneer het uitvoeren van Adobe Analytics, zorg ervoor dat u paginameningen van verbinding het volgen vraag onderscheidt. Bekijk de volgende vraag voor elke interactie die een gebruiker op uw site kan uitvoeren:

*Wanneer een gebruiker met mijn plaats in wisselwerking staat, verandert die interactie genoeg van de inhoud op de pagina om als nieuwe pagina te kwalificeren?*

* Als het antwoord **ja** kunt u een aanroep voor het bijhouden van een paginaweergave gebruiken (`s.t()`).
* Als het antwoord **nee**, overweeg het volgen van die interactie gebruikend een verbinding het volgen vraag (`s.tl()`).

>[!NOTE]
>
>Niet alle interactie of klikken hoeven te worden geregistreerd. Overweeg zorgvuldig welke acties het belangrijkst zijn om te volgen, en gegevens naar Adobe dienovereenkomstig te verzenden.

## Variabelen op elke pagina wissen

De waarden van de variabele blijven op pagina&#39;s AJAX omdat de pagina niet opnieuw wordt geladen. Daarom is speciale accommodatie vereist om variabelewaarden te wissen, zodat deze niet onjuist blijven bestaan in verschillende hits. Adobe biedt de [`clearVars`](../vars/functions/clearvars.md) om de waarden van variabelen gemakkelijk te wissen. Zorg ervoor dat u deze functie gebruikt nadat u elke hit naar de Adobe hebt verzonden en voordat u de variabelewaarden voor de volgende hit instelt.

>[!TIP]
>
>De `clearVars()` functie is niet beschikbaar in H Code. Als u niet hebt bijgewerkt naar AppMeasurement, stelt u elke variabelewaarde van de analysemogelijkheid in op een lege tekenreeks.

## Voorbeelden

In het volgende voorbeeld wordt gebruikgemaakt van eenvoudige JavaScript om bestaande variabelewaarden te wissen, nieuwe waarden in te stellen en vervolgens een afbeeldingsaanvraag naar de Adobe te verzenden:

```js
s.clearVars();
s.pageName = "Example AJAX page";
s.eVar1="Example value";
void(s.t());
```

Het volgende voorbeeld toont een volgende vraag in `done` callback van het JQuery `.ajax` functie:

```js
$.ajax({
  url: "example.html",
  dataType: "html"
})
  .done(function( response ) {
    $( "#content" ).html( response );
  s.clearVars();
  s.pageName = $( "h1:first" ).text();
  s.t();
  });
```
