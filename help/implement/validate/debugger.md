---
title: Oudere Adobe Experience Cloud Debugger
description: Installeer de verouderde foutopsporing voor Adobe Experience Cloud. Dit foutopsporingsprogramma controleert tags voor Analytics, Target, Advertising Cloud, Identity Service, DTM en Launch.
translation-type: tm+mt
source-git-commit: 819f719c4ce131c04916f3b668bcbda1a1b03651

---


# Oudere Adobe Experience Cloud Debugger

> [!IMPORTANT] Dit foutopsporingsprogramma wordt niet meer onderhouden. Adobe raadt u aan in plaats daarvan de [Adobe Experience Cloud Debugger Chrome Extension](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html)te gebruiken.

De [!UICONTROL Legacy Debugger] controletags voor de meeste Adobe Experience Cloud-services. Met het foutopsporingsprogramma kunt u zien welke gegevens op een bepaalde pagina op uw site naar Adobe worden verzonden. U kunt deze informatie gebruiken om de implementatie van uw organisatie problemen op te lossen of te bevestigen.

## De verouderde foutopsporing installeren

Maak een JavaScript-bladwijzer om het foutopsporingsprogramma te installeren.

### Stap 1: Bladwijzercode kopiëren

Kopieer de volgende code naar het klembord:

```JavaScript
javascript:void(window.open("","stats_debugger","width=800,height=800,location=0,menubar=0,status=1,toolbar=0,resizable=1,scrollbars=1").document.write("<script language=\"JavaScript\" id=dbg src=\"https://www.adobetag.com/d1/digitalpulsedebugger/live/DPD.js\"></"+"script>"+"<script language=\"JavaScript\">window.focus();</script>"));
```

### Stap 2: Bladwijzercode in een bladwijzer plakken

Elke browser heeft verschillende manieren om bladwijzers af te handelen, maar het concept is hetzelfde. Er wordt een bladwijzer gemaakt met de gewenste naam en de bladwijzercode als URL.

#### Chroom

Als u erop aandringt om de [chroomuitbreiding](https://docs.adobe.com/content/help/en/debugger/using/experience-cloud-debugger.html)niet te gebruiken, kan de erfenisdebugger boekenmarklet in plaats daarvan worden gebruikt.

1. Klik op de drie stippen in de rechterbovenhoek en ga naar Bladwijzers > Bladwijzerbeheer. U kunt ook op `Ctrl` + `Shift` + `O` (Windows) of `Cmd` + `Shift` + `O` (Mac) drukken.
2. Rechtsboven in de bladwijzermanager klikt u op de drie stippen en vervolgens op Nieuwe bladwijzer toevoegen.
3. Typ in het veld Naam de naam &quot;Adobe Experience Cloud Debugger&quot; en plak het codefragment in het veld URL.
4. Plaats de nieuwe bladwijzer met behulp van bladwijzerbeheer op de gewenste locatie.

#### Firefox

1. Klik op de drie regels rechtsboven en ga naar Bibliotheek > Bladwijzers > Alle bladwijzers tonen. U kunt ook op `Ctrl` + `Shift` + `B` (Windows) of `Cmd` + `Shift` + `B` (Mac) drukken.
2. Klik op Indelen > Nieuwe bladwijzer.
3. Geef in het veld Naam de naam &quot;Adobe Experience Cloud Debugger&quot; en plak het codefragment in het veld Locatie. De tags en trefwoordvelden zijn niet vereist.
4. Plaats uw nieuwe bladwijzer in het bibliotheekvenster op de gewenste locatie.

#### Rand

Edge kan niet handmatig een bladwijzer maken, maar een URL van een bladwijzer kan in een bladwijzer worden bewerkt.

1. Klik op het sterpictogram aan de rechterkant van het URL-veld om een bladwijzer te maken van de huidige pagina.
2. Geef de bladwijzer &quot;Adobe Experience Cloud Debugger&quot; een naam en sla deze op de gewenste locatie op.
3. Klik op het sterpictogram met lijnen om de balk Favorieten te openen.
4. Klik met de rechtermuisknop op de nieuwe bladwijzer en selecteer URL bewerken.
5. Plak het codefragment in het tekstveld en kies Enter.

#### Safari

Safari kan niet handmatig een bladwijzer maken, maar een URL van een bladwijzer kan worden bewerkt in een bladwijzer.

1. Klik op het pictogram Delen in de rechterbovenhoek om een modaal venster van een bladwijzer te openen.
2. Geef de bladwijzer &quot;Adobe Experience Cloud Debugger&quot; een naam en sla deze op de gewenste locatie op.
3. Klik op Bladwijzers > Bladwijzers bewerken en zoek de nieuwe bladwijzer.
4. Klik met de rechtermuisknop > Adres bewerken en plak het codefragment in het tekstveld.

## Het gebruiken van erfenisdebugger

Navigeer naar de gewenste pagina op uw site en klik vervolgens op de bladwijzer. Er wordt een pop-upvenster weergegeven met de gegevens die naar Adobe zijn verzonden.

> [!NOTE] Bepaalde insteekmodules voor het blokkeren van advertenties en pop-upblokkeringen kunnen het laden van het foutopsporingsvenster beïnvloeden. Controleer op geblokkeerde pop-ups in uw browser en sta deze toe zodat de foutopsporing correct werkt.

Debugger heeft verscheidene beschikbare opties, die allen aanpassen hoe het gegeven wordt getoond. Geen van deze opties is van invloed op de gegevensverzameling.

* **Weergegeven producten uit de cloud:** Hiermee toont of verbergt u afbeeldingsaanvragen voor elk respectievelijke Experience Cloud-product.
* **URL-decodering:** URL decodeert de afbeeldingsaanvraag zodat deze overeenkomt met wat wordt weergegeven in de rapportage. Adobe raadt u aan dit selectievakje ingeschakeld te laten.
* **Automatisch vernieuwen:** Hiermee wordt de pop-up elke paar seconden automatisch vernieuwd om te controleren op meer afbeeldingsaanvragen op de pagina. Als u inhoud in debugger moet kopiëren/kleven, maak auto-verfrist onbruikbaar zodat uw selectie blijft.
* **Friendly Format:** Hiermee schakelt u de weergave-indeling tussen handige labels en onbewerkte queryreeksen in een afbeeldingsaanvraag. Zie de parameters [van de de inzamelingsvraag van](query-parameters.md) Gegevens voor meer informatie.

Als u de standaardweergaveopties voor foutopsporing wilt opslaan, klikt u met de rechtermuisknop op de koppeling &#39;Adobe Debugger&#39; in de rechterbovenhoek en kopieert u het koppelingsadres. Bewerk de huidige foutopsporingsbladwijzer en plak het bijgewerkte codefragment in het URL-veld.
