---
title: PWA voor Analytics
description: Progressieve webapps voor Adobe Analytics
role: User, Admin
exl-id: f28e0bfc-0e3e-4f28-9533-6788a36d37fe
source-git-commit: a9d892ab8caaeb797fbbd9b5aa136c5dab76f8bd
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# PWA voor Adobe Analytics

Deze pagina beschrijft hoe u Adobe Analytics kunt gebruiken met Progressieve Web Apps (PWA).

## Inleiding

PWA kunnen een eigen app-ervaring en offline mogelijkheden voor een website bieden. Meestal omvatten PWA een de dienstarbeider, caching bepalingen, en een duidelijk dossier, die allen met snellere ladingstijden, gemakkelijkere navigatie, en ontvankelijk gedrag kunnen helpen.

Adobe Analytics werkt net zo naadloos met PWA als met traditionele websites. Hoewel de PWA nog een paar eisen stellen om zich geleidelijk in en van zich te gedragen, creëren zij geen barrières of beperkingen op de manier waarop Analytics gegevens van hen verzamelt of rapporteert anders dan traditionele websites. Omdat Analytics al mogelijkheden voor offline bijhouden bevat, kunnen PWA u helpen deze ingebouwde functie eenvoudiger te gebruiken dan met traditionele websites.

## Uw PWA Analytics-gegevens ophalen

Als u uw PWA-gegevens wilt verzamelen en analyseren met [!UICONTROL Analytics], hoeft u geen configuratiewijzigingen aan te brengen. [!UICONTROL Analytics] biedt automatisch dezelfde functionaliteit en functies als bij een traditionele website.

## Offline bijhouden toevoegen om de doeltreffendheid van PWA te verhogen

U kunt de doeltreffendheid van uw PWA verhogen door Adobe Analytics [offlinetraceringsmogelijkheden](/help/implement/vars/config-vars/trackoffline.md) met het te gebruiken. Deze functie is standaard uitgeschakeld, maar u kunt de volgende eigenschap toevoegen aan het bestand AppMeasurement.js om deze in te schakelen: `s.trackOffline=true;`.

Bijvoorbeeld, in het volgende dossier AppMeetings.js, wordt het bezit toegevoegd aan het eind van `CONFIG SECTION`:

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

Voor meer informatie over het vormen van het dossier AppMeasurement.js, zie [Overzicht van de variabelen van de Configuratie](/help/implement/vars/config-vars/configuration-variables.md) en de individuele variabelespecifieke pagina&#39;s in het zelfde subhoofdstuk.

Voor meer informatie over de kenmerken van het dossier AppMeasurement.js, zie [overzicht van de implementatie JavaScript](/help/implement/js/overview.md).
