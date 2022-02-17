---
title: PWA voor Analytics
description: Progressieve webapps voor Adobe Analytics
role: User, Admin
feature: Progressive Web Apps
exl-id: f28e0bfc-0e3e-4f28-9533-6788a36d37fe
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
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

Om uw PWA gegevens met te verzamelen en te analyseren [!UICONTROL Analytics]hoeft u geen configuratiewijzigingen aan te brengen. [!UICONTROL Analytics] biedt automatisch dezelfde functionaliteit en functies als bij een traditionele website.

## Offline bijhouden toevoegen om de doeltreffendheid van PWA te verhogen

U kunt de effectiviteit van uw PWA verhogen door Adobe Analytics te gebruiken [mogelijkheden voor offline bijhouden](/help/implement/vars/config-vars/trackoffline.md) ermee. Deze functie is standaard uitgeschakeld, maar u kunt de volgende eigenschap toevoegen aan het bestand AppMeasurement.js om deze in te schakelen: `s.trackOffline=true;`.

In het volgende bestand AppMeturement.js wordt de eigenschap bijvoorbeeld toegevoegd aan het einde van het dialoogvenster `CONFIG SECTION`:

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

Zie voor meer informatie over het configureren van het bestand AppMeasurement.js [Overzicht van configuratievariabelen](/help/implement/vars/config-vars/configuration-variables.md) en de afzonderlijke variabelespecifieke pagina&#39;s in hetzelfde subhoofdstuk.

Voor meer informatie over de kenmerken van het bestand AppMeasurement.js raadpleegt u de [Overzicht van JavaScript-implementatie](/help/implement/js/overview.md).
