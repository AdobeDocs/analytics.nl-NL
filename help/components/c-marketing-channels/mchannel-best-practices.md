---
title: Aanbevolen procedures voor het implementeren van Adobe Analytics Marketing Channel
description: Bijgewerkte beste praktijken voor het gebruiken van de Kanalen van de Marketing met Attributie en Customer Journey Analytics
feature: Marketing Channels
exl-id: a0ab818d-7165-4f34-bc43-1ed8d6215800
source-git-commit: 16fdad50b9d63bc6db07347c6ec91fb0d2df5722
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---

# Attributie met de Kanalen van de Marketing - Beste praktijken

[ de Kanalen van de Marketing ](/help/components/c-marketing-channels/c-getting-started-mchannel.md) zijn een waardevolle en krachtige eigenschap van Adobe Analytics. De huidige begeleiding betreffende de implementatie van het Kanaal van de Marketing werd geformuleerd in een tijd toen noch [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) noch [ Customer Journey Analytics ](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-usecases/marketing-channels.html#cja-usecases) bestond.

Om de implementatie van uw marketingkanalen in de toekomst te controleren en ervoor te zorgen dat de rapportage consistent is met Attribution en met Customer Journey Analytics, geven we een reeks bijgewerkte best practices uit. Als u al marketingkanalen gebruikt, kunt u de beste opties kiezen uit deze nieuwe richtlijnen. Als u niet bekend bent met Marketing Channels, raden we u aan alle nieuwe aanbevolen procedures te volgen.

Toen de Kanalen van de Marketing voor het eerst werden geïntroduceerd, kwamen zij met slechts eerste-aanraak en last-aanraking dimensies. Expliciete eerste/laatste aanraakafmetingen zijn niet meer nodig met de huidige versie van de toewijzing. Adobe biedt algemene &#39;Marketing Channel&#39;- en &#39;Marketing Channel Detail&#39;-afmetingen, zodat u deze kunt gebruiken met het gewenste attributiemodel. Deze generische afmetingen gedragen zich identiek aan de laatste-aanraak afmetingen van het Kanaal, maar verschillend geëtiketteerd om verwarring te verhinderen wanneer het gebruiken van de Kanalen van de Marketing met een verschillend attributiemodel.

Aangezien de dimensies van het Kanaal van de Marketing van een traditionele definitie van het Bezoek (zoals die door hun verwerkingsregels wordt bepaald) afhangen, kan hun definitie van het Bezoek niet worden veranderd gebruikend virtuele rapportreeksen. Deze herziene praktijken laten duidelijke en gecontroleerde raadplegingsvensters met Attributie en met Adobe Analytics toe.

## Beste praktijken #1: De Attributie van de hefboomwerking voor gecontroleerde analyse

Wij adviseren gebruikend [ Attributie ](/help/analyze/analysis-workspace/attribution/overview.md) in plaats van de bestaande attributie van het Kanaal van de Marketing om uw analyse van het Kanaal van de Marketing te verfijnen. Volg de andere beste praktijken om consistentie en robuuste controles over uw analyse met Attributie te verzekeren.

![](assets/attribution.png)

* De configuratie van de dimensies van het Kanaal van de Marketing en het Detail van het Kanaal van de Marketing vestigt te evalueren aanraakpunten, die aan elke Instantie van het Kanaal van de Marketing beantwoorden.
* Voor metrische analyse, zou uw organisatie zich op één of meerdere attributiemodel(en) moeten richten. Sla aangepaste maateenheden op met dit model, zodat u ze eenvoudig opnieuw kunt gebruiken.
* Standaard worden gegevens toegewezen met gebruik van Last Touch en de instelling van de bezoekersperiode. De metrische modellen van de attributie bieden grotere controle over de raadplegingsvensters en meer verscheidenheid, met inbegrip van [ algoritmische attributie ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/attribution/algorithmic.html#analysis-workspace) aan.

## Beste praktijken #2: Geen Directe en Zitting verfrissen kanaaldefinities

De directe en Interne kanalen van het Sessievernieuwen worden niet geadviseerd voor gebruik met de modellen van de douaneattributie.

Wat als uw organisatie reeds Directe en Zitting heeft gevormd verfrissen zich? In dit geval, adviseren wij dat u [ een classificatie ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/classifications-mchannel.md) voor Eerste Aanraak/Laatste Aanraak creeert en Direct en Zitting verfrist kanalen niet geclassificeerd verlaat. De geclassificeerde dimensie zal de zelfde resultaten van de Attributie opleveren alsof die kanalen nooit werden gevormd.

![](assets/direct-session-refresh.png)

## Best practice #3: Enable Override Last-Touch Channel voor alle kanalen

Aangepaste toewijzingsmodellen die worden gebruikt met de dimensie Marketing Channel in Workspace, werken het beste als deze instelling is ingeschakeld. Als u deze instelling inschakelt, telt een marketingkanaalinstantie wanneer een nieuw kanaal/detail wordt aangetroffen. Schakel deze optie in voor alle kanalen behalve Direct of Intern/Sessie vernieuwen, die we niet langer aanbevelen voor gebruik met aangepaste attributiemodellen.

![](assets/override.png)

## Beste praktijken #4: Minimaliseer de periode van de Aanwezigheid van de Bezoeker

Door de bedenktijd van de bezoeker in te stellen op het minimum van &quot;1 dag&quot; minimaliseert u de kans op het vasthouden van waarden. Omdat de modellen van de douaneattributie (AIQ) flexibele raadplegingsvensters toestaan, adviseren wij plaatsend de minimumwaarde om het effect van deze het plaatsen te minimaliseren.

![](assets/expiration.png)

## Beste praktijken #5: De Verwerkingsregels van de Kanalen van de marketing zouden slechts voor toegelaten kanalen moeten bestaan

Zorg ervoor dat u alle regels voor de verwerking van marketingkanalen voor uitgeschakelde kanalen verwijdert. De regels zouden slechts voor de Kanalen van de Marketing moeten bestaan die zoals toegelaten worden gecontroleerd.
