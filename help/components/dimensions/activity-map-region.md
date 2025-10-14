---
title: Activity Map
description: Het gebied op uw site waarop is geklikt.
feature: Dimensions
role: User, Admin
source-git-commit: 05010d58ba2a3376473097e9d4543ee4415e83e1
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 0%

---

# Activity Map

De &quot;Gebied van de Activity Map&quot;[&#x200B; dimensie &#x200B;](overview.md) toont de gebieden op uw plaats die het meest klikte. Deze dimensie is handig wanneer u kliks in overkoepelende gebieden van uw site wilt vergelijken in plaats van afzonderlijke koppelingen. Het is ook handig voor gebieden van uw site die dynamische inhoud leveren. Bijvoorbeeld, als u een voorpagina met het roteren van nieuwsartikelen hebt, zou het gebruiken van de [&#x200B; dimensie van de Verbinding van de Activity Map &#x200B;](activity-map-link.md) moeilijk zijn omdat de verbindingstekst constant verandert. Aangezien deze koppelingen echter hetzelfde gebied gebruiken, kunt u de prestaties van dat gebied analyseren, ook al kunnen afzonderlijke koppelingen elke dag veranderen.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van de [&#x200B; variabele van contextgegevens &#x200B;](/help/implement/vars/page-vars/contextdata.md) terug `c.a.activitymap.region`. Als uw implementatie [&#x200B; Activity Map &#x200B;](/help/analyze/activity-map/overview.md) gebruikt, verzamelt deze variabele van contextgegevens automatisch gegevens wanneer de verbindingen worden geklikt.

Controleer voor een bepaalde koppeling waarop is geklikt het bovenliggende DOM-element op het volgende (in volgorde):

* Een waarde in het kenmerk ingesteld door [`ActivityMap.regionIDAttribute`](/help/implement/vars/config-vars/activitymap-regionidattribute.md) - standaard ingesteld op het kenmerk `id`
* Een waarde in het kenmerk `aria-label` wanneer het kenmerk `role="region"`
* De semantische elementen `<header>`, `<main>`, `<footer>` of `<nav>` (alleen Web SDK)

Als het bovenliggende DOM-element niet aan een van de bovenstaande criteria voldoet, wordt de zoekopdracht recursief uitgevoerd in de DOM-hiërarchie. Wanneer geen overeenkomende elementen worden gevonden, wordt de waarde `BODY` geretourneerd.

## Dimension-items

Dimension-items bevatten gebieden die op uw site van een label zijn voorzien. De waarden van specifieke gebieden hangen af van welke kenmerken worden gebruikt en of er semantische HTML-elementen aanwezig zijn.
