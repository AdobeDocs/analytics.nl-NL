---
title: Veelgestelde vragen over de implementatie van Analytics
description: Veelgestelde vragen over implementatie en koppelingen naar meer informatie.
keywords: Analytics Implementation;faq;frequently asked questions;evar expiration;custom event visibility;timestamp;visitor id grace period;visitor id;Experience Cloud visitor id;analytics visitor id;dtm;heartbeat;cookies;tracking server;performance;javascript;data collection;s_code version;s_code debug;track link types;track video;track mobile app;first party cookie;ssl certificate;certification expiration;certificate expiration;plugins;data insertion api;500 error;500;Manage user;manage group;users;groups
translation-type: ht
source-git-commit: d1db8da65faac1bf09fa2a290a2645092b542a35

---


# Veelgestelde vragen over de implementatie van Analytics

Veelgestelde vragen over implementatie en koppelingen naar meer informatie.

**Wat is het verschil tussen variabele toewijzing en vervaldatum?**

Toewijzing en vervaldatum zijn allebei instellingen die u kunt toepassen op aangepaste variabelen. *Toewijzing* vindt plaats wanneer u een permanente waarde voor een variabele en een nieuwe waarde voor een variabele hebt. Hiermee wordt bepaald of de oude waarde of de nieuwe waarde behouden blijft. *Vervaldatum* komt aan de orde wanneer u een variabele waarde niet wilt behouden.

**Wat is het verschil tussen de Experience Cloud-bezoekers-ID en de Analytics-bezoekers-ID?**

De Identity Service wijst een unieke, permanente id toe die kan worden gedeeld tussen andere oplossingen in de Experience Cloud. De bezoekers-ID van Analytics wordt alleen gebruikt door Analytics. Adobe raadt u aan de Experience Cloud-bezoekers-ID te gebruiken in uw implementatie.

**Hoe wordt een bezoekers-ID ingesteld als cookies zijn geblokkeerd?**

Als het standaardcookie `s_vi` niet beschikbaar is, wordt op het domein van de website een fallback-cookie gemaakt met een willekeurig gegenereerde unieke id. Dit cookie, genaamd `s_fid`, wordt ingesteld met een vervaldatum van 2 jaar en wordt gebruikt als de toekomstige fallback-identificatiemethode.

**Hoe kan ik momentopnamen van videotracering implementeren?**

Zie [Audio en video meten in Adobe Analytics](https://docs.adobe.com/content/help/nl-NL/media-analytics/using/media-overview.html).

**Kan een onderbreking van de service bij Adobe de prestaties beïnvloeden?**

Nee. Het JavaScript-bestand wordt niet op Adobe-servers gehost, dus een Adobe-storing heeft geen invloed op uw AppMeasurement-bibliotheek. Als u Adobe Experience Platform Launch gebruikt, wordt het JavaScript-bestand gehost door Akamai of op een door uw organisatie bepaalde serverlocatie.

**Kan het verzenden van data van de browser naar Adobe-services de prestaties verminderen?**

AppMeasurement maakt een afbeeldingsobject binnen de HTML-pagina en de browser vraagt het afbeeldingsobject vervolgens op bij Adobe-servers voor dataverzameling. Als de servers voor dataverzameling traag of niet antwoorden, wordt de thread waarin de aanvraag wordt behandeld, vertraagd totdat de afbeelding terugkomt of een time-out optreedt. Omdat browsers afbeeldingen met meerdere threads verwerken, heeft een Adobe-stroomstoring een minimale invloed op de laadtijd van de pagina. Hierdoor wordt één thread vastgezet terwijl de andere threads actief blijven.

**Hoe kan ik een mobiele app traceren?**

U kunt de Adobe Experience Platform-SDK gebruiken. Zie [Overzicht van Adobe Experience Platform-SDK](https://aep-sdks.gitbook.io/docs/) voor meer informatie.

**Wat zijn plug-ins?**

Plug-ins zijn codefragmenten die geavanceerde functies uitvoeren. Ze breiden de mogelijkheden van AppMeasurement uit om uw implementatie meer functionaliteit te geven.
