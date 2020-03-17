---
description: Toont de gemeenschappelijkste verbindingen mensen op klikken die tot plaatsen buiten uw plaats leiden. Deze verbindingen richten typisch aan partner of verwante plaatsen. Ze kunnen echter elke locatie zijn waar u een externe koppeling hebt geïmplementeerd. U kunt dit rapport gebruiken om de populairste partnerverbindingen te bekijken, of bij het bevestigen van het aantal verwijzingen te helpen die de staat van uw partners u verstrekt.
title: Koppelingen afsluiten
topic: Reports
uuid: e1452f04-389d-4aa3-8763-732880284302
translation-type: tm+mt
source-git-commit: ''

---


# Koppelingen afsluiten

Toont de gemeenschappelijkste verbindingen mensen op klikken die tot plaatsen buiten uw plaats leiden. Deze verbindingen richten typisch aan partner of verwante plaatsen. Ze kunnen echter elke locatie zijn waar u een externe koppeling hebt geïmplementeerd. U kunt dit rapport gebruiken om de populairste partnerverbindingen te bekijken, of bij het bevestigen van het aantal verwijzingen te helpen die de staat van uw partners u verstrekt.

Deze pagina kan alleen correct worden ingevuld als aan verschillende vereisten is voldaan:

* Als het gebruiken van het handspoor van de douaneverbinding, een *`s.tl()`* verzoek moet met de middelste parameter worden in brand gestoken die aan *e* wordt geplaatst.

* Als u automatische aangepaste koppelingencontrole gebruikt, moet aan alle vereisten worden voldaan:
* 

   * [s.trackExternalLinks](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_trackexlinks.html) moet zijn ingesteld op *true*.

   * De koppeling waarop de gebruiker heeft geklikt, mag niet overeenkomen met waarden binnen de variabele [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_linkinfilters.html) .
   * Als [s.linkInternalFilters](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_linkinfilters.html) wordt uitgevoerd, moet de externe verbinding minstens één van de waarden aanpassen die in deze variabele worden geplaatst.

* Als aan een van de bovenstaande voorwaarden niet wordt voldaan, wordt dit rapport niet ingevuld.

* 
* Net als bij alle aangepaste resultaten bij het bijhouden van koppelingen, wordt de variabele [s.pageName](https://marketing.adobe.com/resources/help/en_US/sc/implement/c_pagename.html) uit de afbeeldingsaanvraag verwijderd om inflatie in de paginaweergave te voorkomen.
* U kunt dit rapport weergeven in een georiënteerde en gerangschikte indeling.
* Dit rapport kan een onderzoeksfilter gebruiken om van specifieke lijnpunten de plaats te bepalen.
* U kunt [onderverdelingen](/help/analyze/reports-analytics/reports-customize/breakdowns.md) maken met elke andere variabele via Admin Tools.
* [De instanties](/help/components/c-variables/c-metrics/metrics-instance.md) zijn de enige metriek beschikbaar door gebrek binnen dit rapport, tellend het aantal tijden de uitgangsverbinding in brand gestoken.
* Voor dit rapport kunnen dagelijkse, wekelijkse, maandelijkse en driemaandelijkse bezoekers worden ingeschakeld. Alleen een vertegenwoordiger van Adobe kan dit echter tegen extra kosten inschakelen. Het toelaten van unieke bezoekers voor om het even welke variabelen van het douanecontracten verhoogt zeer latentie voor de rapportreeks.

