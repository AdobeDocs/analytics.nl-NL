---
title: Implementeren met AJAX
description: Leer hoe u Adobe Analytics implementeert op een site met AJAX.
translation-type: tm+mt
source-git-commit: dabaf6247695bc4f3d9bfe668f3ccfca12a52269

---


# Implementeren met AJAX

AJAX is een manier om JavaScript en HTML te gebruiken om inhoud te wissen en te genereren zonder een nieuwe pagina te laden.

Adobe Analytics is meestal afhankelijk van pagina&#39;s die opnieuw worden geladen om het object Analytics tracking opnieuw in te stellen. Elke keer dat u naar een andere URL navigeert, worden alle variabelen voor Analytics opnieuw ingesteld en kunnen deze opnieuw worden gedefinieerd. Wanneer u AJAX op uw site gebruikt, past u de implementatie aan rond het ontbreken van pagina-vernieuwingen om ervoor te zorgen dat gegevens niet onjuist blijven bestaan tussen treffers.

Als u maatregelen hebt ingesteld om variabele waarden te wissen, is het implementeren van Adobe Analytics op sites die AJAX gebruiken meestal hetzelfde als andere implementatiemethoden.

## Interacties en raaktypen bepalen

Aangezien pagina&#39;s die AJAX gebruiken doorgaans niet opnieuw worden geladen, kan een gebruiker meerdere interacties op uw site uitvoeren. Wanneer het uitvoeren van de Analyse van Adobe, zorg ervoor dat u paginameningen van verbinding het volgen vraag onderscheidt. Bekijk de volgende vraag voor elke interactie die een gebruiker op uw site kan uitvoeren:

*Wanneer een gebruiker met mijn plaats in wisselwerking staat, verandert die interactie genoeg van de inhoud op de pagina om als nieuwe pagina te kwalificeren?*

* Als het antwoord **ja** is, overweeg het gebruiken van een pagina mening het volgen vraag (`s.t()`).
* Als het antwoord **neen** is, overweeg het volgen van die interactie gebruikend een verbinding het volgen vraag (`s.tl()`).

>[!NOTE] Niet alle interactie of klikken hoeven te worden geregistreerd. Overweeg zorgvuldig welke handelingen het belangrijkste zijn om te volgen en stuur gegevens naar Adobe.

## Variabelen op elke pagina wissen

Variabele waarden blijven aanwezig op pagina&#39;s die AJAX gebruiken, omdat de pagina niet opnieuw wordt geladen. Daarom is speciale accommodatie vereist om variabelewaarden te wissen, zodat deze niet onjuist blijven bestaan in verschillende hits. Adobe biedt de [`clearVars`](../vars/functions/clearvars.md) functie om variabele waarden gemakkelijk te wissen. Zorg ervoor dat u deze functie gebruikt nadat u elke hit naar Adobe hebt verzonden en voordat u waarden voor variabelen instelt voor de volgende hit.

>[!TIP] De `clearVars()` functie is niet beschikbaar in H Code. Als u niet hebt bijgewerkt naar AppMeasurement, stelt elke waarde van de variabele Analytics in op een lege tekenreeks.

## Voorbeelden

In het volgende voorbeeld wordt gebruikgemaakt van eenvoudige JavaScript om bestaande variabelewaarden te wissen, nieuwe waarden in te stellen en vervolgens een aanvraag voor een afbeelding naar Adobe te verzenden:

```js
s.clearVars();
s.pageName = "Example AJAX page";
s.eVar1="Example value";
void(s.t());
```

Het volgende voorbeeld toont een volgende vraag in de `done` callback van de functie JQuery `.ajax` :

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
