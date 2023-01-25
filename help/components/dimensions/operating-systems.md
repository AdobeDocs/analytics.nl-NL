---
title: Besturingssysteem
description: Het besturingssysteem van de bezoeker.
feature: Dimensions
exl-id: e3911ae0-d242-4da2-a4bc-b2f4877f9dd2
source-git-commit: 17c441f8855b8ca0604076763817de8d4d3b8efb
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Besturingssysteem

De dimensie &#39;Besturingssysteem&#39; geeft het besturingssysteem en de versie weer die de bezoeker heeft gebruikt. Als u functies in uw webeigenschap hebt die OS-specifiek zijn, kunt u met deze dimensie beter begrijpen welke besturingssystemen het meest worden gebruikt.

## Deze dimensie vullen met gegevens

Deze dimensie verwijst naar een raadplegingstabel intern aan Adobe. De opzoekwaarde is gebaseerd op de `User-Agent` HTTP-header in afbeeldingsaanvragen. Als u een AppMeasurement-bibliotheek gebruikt (bijvoorbeeld via tags in Adobe Experience Platform), werkt deze dimensie buiten het vak.

## Dimension-items

Dimension-items omvatten besturingssystemen die bezoekers gebruiken. Voorbeelden zijn `"Windows 10"`, `"OS X 10.15"`, en `"Android 9"`.

## Wijzigingen in etikettering en definitie

Hieronder volgt een lijst met specifieke problemen met de manier waarop het besturingssysteem is vertegenwoordigd in de gebruikersagent en in Adobe Analytics-rapportage.

### Wijzigen in naamgevingsconventie voor Apple-besturingssysteem:

Vanaf versie 11 gebruiken we MacOS in plaats van OS X om naar het Apple-besturingssysteem te verwijzen.

Voorbeelden:

* &quot;OS X 10.15&quot; (zie opmerking hieronder over versie 10.15.7 over representatie in UA-tekenreeksen).
* &quot;MacOS 11.0.0

### Mac OS-versie is onjuist in de gebruikersagent na versie 10.15.7 

De gebruikersagent op Apple-computers geeft de versie van het besturingssysteem weer op 10.15.7, zelfs als het een nieuwere versie betreft. Dit is gebeurd omdat het opnemen van versie 11 in de UA blijkbaar problemen heeft veroorzaakt met sommige websites. Dit geldt voor *alle browsers* en heeft geen betrekking op het &#39;bevriezen&#39; van de gebruikersagent in Chromium-browsers door de Google.

Clienthints bevatten de juiste versie in de hint van de platformversie (&quot;Sec-CH-UA-Platform-Version&quot;). Dit is een hoge entropiehint zodat deze niet automatisch door Adobe wordt verzameld. Zie de [Veelgestelde vragen over Adobe Analytics Hints](https://experienceleague.adobe.com/docs/analytics/technotes/client-hints.html?lang=en) voor meer informatie over het verzamelen van hoge entropiehints.

### De versie van Windows is onjuist in de gebruikersagent die begint met Windows 11

Vanaf januari 2023 vertegenwoordigt de gebruikersagent in alle browsers Windows 11 als Windows 10.

Clienthints bevatten de juiste versie in de hint van de platformversie (&quot;Sec-CH-UA-Platform-Version&quot;). Dit is een hoge entropiehint zodat deze niet automatisch door Adobe wordt verzameld. Zie de [Veelgestelde vragen over Adobe Analytics Hints](https://experienceleague.adobe.com/docs/analytics/technotes/client-hints.html?lang=en) voor meer informatie over het verzamelen van hoge entropiehints.
