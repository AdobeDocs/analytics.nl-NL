---
title: Browser
description: De naam en versie van de gebruikte browser.
feature: Dimensions
exl-id: 2bdf2a5a-3482-43fa-b2e1-fbea892918fb
source-git-commit: d095628e94a45221815b1d08e35132de09f5ed8f
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 1%

---

# Browser

De &#39;[!UICONTROL Browser]&#39; [dimensie](overview.md) meldt de naam en versie van de browser die de hit verzendt. Deze dimensie is handig voor het begrijpen van de meest gebruikte browsers die bezoekers gebruiken. Wanneer u nieuwe versies van uw site test, kunt u deze tests uitvoeren in de bovenste browsers in deze dimensie om de inspanningen voor kwaliteitscontrole te maximaliseren.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Als u een bibliotheek met AppMeasurementen gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak.

## Dimension-items

Dimension-items omvatten de gebruikte browsernamen en -versies. Verschillende versies van dezelfde browser zijn afzonderlijke dimensie-items.

Sommige dimensie-items bevatten `"(unknown version)"` in plaats van hun versienummer. Dit afmetingspunt verwijst naar een recente browser versie die de Adobe niet aan hun raadplegingslijsten heeft toegevoegd. Aangezien browsers vaak worden bijgewerkt, worden de `"(unknown version)"` voor een bepaalde browser algemeen en tijdelijk is. Adobe werkt opzoektabellen doorgaans bij tijdens maandelijkse onderhoudsreleases.

## Wijzigingen in etikettering en definitie

Hieronder volgt een lijst met wijzigingen in de manier waarop browsers worden weergegeven in de rapportage. Deze wijzigingen kunnen van invloed zijn op uw rapportage of op elke logica, zoals segmenten, die afhankelijk is van deze waarden.

### Bedrijf uit browser verwijderen

Vanaf versie 100 voor Chrome-, Edge- en Firefox-browsers wordt de bedrijfsnaam niet meer weergegeven voor de browser. Dit kan gevolgen hebben voor gebruikers als zij segmentdefinities hebben die zijn gebaseerd op de naam van de browser. Een segment met een definitie die &#39;browser bevat &#39;Google&#39;, herkent Chrome-browsers die beginnen met versie 110 bijvoorbeeld niet meer.

Voorbeelden:

Versie 109 van Chrome wordt weergegeven als &quot;Google Chrome 109&quot;.
Versie 110 van Chrome wordt weergegeven als &quot;Chrome 109&quot;.

### Het onderscheid tussen mobiel en niet-mobiel voor Chrome verwijderen

Vanaf Chrome 110 worden zowel mobiele als niet-mobiele versies van Chrome van hetzelfde label voorzien. Mobiele en niet-mobiele versies krijgen momenteel een apart label. Belangrijk: hiermee verandert u de betekenis van de naam zonder &quot;mobiel&quot;. Chrome 109 is niet-mobiel (dus bureaublad) &quot;Chrome 110&quot; is mobiel en niet-mobiel. Als u segmentdefinities hebt die verwijzen naar &quot;mobiel&quot; in de naam van de browser, werken deze mogelijk niet meer naar behoren. U kunt mobiele segmentatie en onderbrekingen gebruiken om mobiel aan niet-mobiel verkeer te vergelijken.

Voorbeelden:

Mobiel chroom 109 wordt weergegeven als &quot;Chrome Mobile 109&quot;.
Niet-mobiele chroom 109 wordt weergegeven als &quot;Chrome 109&quot;.

Mobiel chroom 110 wordt weergegeven als &quot;Chrome 110&quot;.
Niet-mobiele chroom 110 wordt weergegeven als &quot;Chrome 110&quot;.
