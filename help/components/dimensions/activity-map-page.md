---
title: Activity Map-pagina
description: De paginanaam wanneer op een koppeling is geklikt.
feature: Dimensions
role: User, Admin
source-git-commit: 72b38970e573b928e4dc4a8c8efdbfb753be0f4e
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 3%

---

# Activity Map-pagina

De &quot;Pagina van de Activity Map&quot;[&#x200B; dimensie &#x200B;](overview.md) toont de pagina die een bezoeker was toen een verbinding werd geklikt. Met deze dimensie kunt u bepalen welke pagina&#39;s koppelingen bevatten waarop het meest wordt geklikt. Deze dimensie wordt ook gebruikt door de overlay Activity Map om te bepalen welke verbindingen aan vertoning.

## Deze dimensie vullen met gegevens

Deze afmeting wint gegevens van de [&#x200B; variabele van contextgegevens &#x200B;](/help/implement/vars/page-vars/contextdata.md) terug `c.a.activitymap.page`. Als uw implementatie [&#x200B; Activity Map &#x200B;](/help/analyze/activity-map/overview.md) gebruikt, verzamelt deze variabele van contextgegevens automatisch gegevens wanneer de verbindingen worden geklikt.

Voor een bepaalde verbinding die werd geklikt, verzamelt deze variabele van contextgegevens de waarde in de [&#x200B; dimensie van de Pagina &#x200B;](page.md). Als de afmeting van de Pagina geen waarde bevat, wordt de [&#x200B; pagina URL &#x200B;](page-url.md) afmeting gebruikt in plaats daarvan (zo gelijkaardig aan de reserve die de afmeting van de Pagina gebruikt). De gegevens van de Activity Map worden typisch verzonden op de volgende klap nadat een verbinding werd geklikt. Met deze dimensie kunt u de paginawaarde bepalen wanneer op de koppeling werd geklikt, in plaats van de paginawaarde wanneer gegevens werden verzonden.

## Dimension-items

De punten van het Dimension omvatten alle waarden die in de [&#x200B; dimensie van de Pagina &#x200B;](page.md) worden gevonden.
