---
title: PWA's voor analyse
description: Progressieve webtoepassingen voor Adobe Analytics
translation-type: tm+mt
source-git-commit: 16ba0b12e0f70112f4c10804d0a13c278388ecc2

---


# PWA&#39;s voor analyse

In deze handleiding wordt beschreven hoe u Adobe Analytics kunt gebruiken met Progressive Web Apps (PWA&#39;s).

## Inleiding

PWA&#39;s kunnen een native app-ervaring en offlinemogelijkheden bieden voor een website. Gewoonlijk omvatten PWAs een de dienstarbeider, caching bepalingen, en een manifestdossier, allen die met snellere ladingstijden, gemakkelijkere navigatie, en ontvankelijk gedrag kunnen helpen.

Adobe Analytics werkt net zo naadloos met PWAs als met traditionele websites. Hoewel PWA&#39;s nog een paar vereisten hebben om zich geleidelijk in en van zichzelf te gedragen, creëren ze geen belemmeringen of beperkingen voor de manier waarop Analytics gegevens van hen verzamelt of rapporteert op een andere manier dan traditionele websites. Omdat Analytics al mogelijkheden voor offline bijhouden bevat, kunnen PWA&#39;s u helpen deze ingebouwde functie eenvoudiger te gebruiken dan met traditionele websites.

## Uw PWA-analysegegevens ophalen

Als u uw PWA-gegevens wilt verzamelen en analyseren met Analytics, hoeft u geen configuratiewijzigingen aan te brengen. Analyses bieden automatisch dezelfde functionaliteit en functies als bij een traditionele website.

## Offline bijhouden toevoegen om de PWA-effectiviteit te verhogen

U kunt de doeltreffendheid van uw PWA verhogen door Analytics [off-line het volgen mogelijkheden](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/offline-tracking.html) met het te gebruiken. Deze functie is standaard uitgeschakeld, maar u kunt de volgende eigenschap toevoegen aan het bestand AppMeasurement.js om deze in te schakelen: `s.trackOffline=true;`.

In het volgende bestand AppMeturement.js wordt de eigenschap bijvoorbeeld toegevoegd aan het einde van het bestand `CONFIG SECTION`:

```
/************************** CONFIG SECTION **************************/ 
/* You may add or alter any code config here. */ 
/* Link Tracking Config */ 
s.trackDownloadLinks=true 
s.trackExternalLinks=true 
s.trackInlineStats=true 
s.linkDownloadFileTypes="exe,zip,wav,mp3,mov,mpg,avi,wmv,pdf,doc,docx,xls,xlsx,ppt,pptx" 
s.linkInternalFilters="javascript:" //optional: add your internal domain here 
s.linkLeaveQueryString=false 
s.linkTrackVars="None" 
s.linkTrackEvents="None" 
s.trackOffline=true
***
    
```


Zie Code [invoegen in het bestand](https://docs.adobe.com/content/help/en/analytics/implementation/implement-analytics-with-dtm/analytics-tool/t-appmeasurement-code.html)AppMeasurement.js voor meer informatie over het bewerken van het bestand AppMeasurement.js.

Voor voorbeelden van configuraties in het dossier AppMeasurement.js, zie het [Vormen van het dossier](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasure-mjs-pagecode.html#section_042412C29CC249E298F19B2BC2F43CE7)AppMeasurement.js.

Voor meer informatie over de kenmerken van het dossier AppMeasurement.js, zie het [implementatieoverzicht](https://docs.adobe.com/content/help/en/analytics/implementation/javascript-implementation/appmeasurement-js/appmeasure-mjs.html)Javascript.
