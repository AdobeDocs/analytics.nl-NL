---
title: Veelgestelde vragen over implementatie van Analytics
description: Veelgestelde vragen over implementatie en koppelingen naar meer informatie.
keywords: Analytics Implementation;faq;frequently asked questions;evar expiration;custom event visibility;timestamp;visitor id grace period;visitor id;Experience Cloud visitor id;analytics visitor id;dtm;heartbeat;cookies;tracking server;performance;javascript;data collection;s_code version;s_code debug;track link types;track video;track mobile app;first party cookie;ssl certificate;certification expiration;certificate expiration;plugins;data insertion api;500 error;500;Manage user;manage group;users;groups
translation-type: tm+mt
source-git-commit: ''

---


# Veelgestelde vragen over implementatie van Analytics

Veelgestelde vragen over implementatie en koppelingen naar meer informatie.

**Wat is het verschil tussen variabele toewijzing en vervaldatum?**

Toewijzing en vervaldatum zijn beide instellingen die u kunt toepassen op aangepaste variabelen. *Toewijzing* vindt plaats wanneer u een waarde hebt die bestaat uit een permanente variabele en een nieuwe waarde voor de variabele. Hiermee wordt bepaald of de oude waarde of de nieuwe waarde behouden blijft. *De vervaldatum* wordt in werking gesteld wanneer u niet een veranderlijke waarde wilt voortzetten hardend.

**Wat is het verschil tussen de Experience Cloud bezoeker-id en de Analytics-bezoeker-id?**

De Identity Service wijst een unieke, permanente id toe die kan worden gedeeld door andere oplossingen in de Experience Cloud. De bezoeker-id van Analytics wordt alleen gebruikt door Analytics. Adobe raadt u aan de Experience Cloud Visitor ID Service te gebruiken in uw implementatie.

**Hoe wordt een bezoeker-id ingesteld als cookies worden geblokkeerd?**

Als het standaardcookie niet beschikbaar is, wordt een fallback-cookie gemaakt op het domein van de website met een willekeurig gegenereerde unieke id. `s_vi` Dit cookie, genaamd `s_fid`, wordt ingesteld met een vervaldatum van 2 jaar en wordt gebruikt als de fallback-identificatiemethode die op de volgende datum wordt gebruikt.

**Hoe kan ik hartslagvideo bijhouden implementeren?**

Zie Audio en video [meten in Adobe Analytics](https://docs.adobe.com/content/help/en/media-analytics/using/media-overview.html).

**Kan een onderbreking van de service bij Adobe de prestaties beïnvloeden?**

Nee. Het JavaScript-bestand wordt niet op Adobe-servers gehost, dus een Adobe-storing heeft geen invloed op uw AppMeasurement-bibliotheek. Als u Adobe Experience Platform Launch gebruikt, wordt het JavaScript-bestand gehost door Akamai of op een door uw organisatie bepaalde serverlocatie.

**Kan het verzenden van gegevens van de browser naar Adobe-services de prestaties verminderen?**

AppMeasurement maakt een afbeeldingsobject binnen de HTML-pagina en de browser vraagt het afbeeldingsobject vervolgens op bij Adobe-servers voor gegevensverzameling. Als de servers van de gegevensinzameling langzaam waren of niet antwoordden, zou de draad behandeling die verzoek worden vertraagd tot het beeld terugkeert of een onderbreking voorkomt. Omdat browsers afbeeldingen met meerdere threads verwerken, heeft een Adobe-stroomstoring een minimale invloed op de laadtijd van de pagina. Hierdoor wordt een thread gekoppeld terwijl de andere thread actief blijft.

**Hoe kan ik een mobiele app bijhouden?**

U kunt de SDK van het Adobe Experience Platform gebruiken. Zie Overzicht [van](https://aep-sdks.gitbook.io/docs/) Adobe Experience Platform voor meer informatie.

**Wat zijn plug-ins?**

Plug-ins zijn codefragmenten die geavanceerde functies uitvoeren. Zij breiden de mogelijkheden van AppMeasurement uit om uw meer functionaliteit in uw implementatie te geven.
