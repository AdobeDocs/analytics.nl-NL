---
title: Koppelingen afsluiten
description: Rapport over de meest gebruikte koppelingen waarop mensen klikken om uw site te verlaten.
translation-type: tm+mt
source-git-commit: be4c3ec95b9e93dda7603c0bdb178c0a54d800a0

---


# Koppelingen afsluiten

Toont de gemeenschappelijkste verbindingen mensen zijn klikken om uw plaats te verlaten. Deze verbindingen richten typisch aan partner of verwante plaatsen; ze kunnen echter elke locatie zijn waar u een externe koppeling hebt. U kunt dit rapport gebruiken om de populairste partnerverbindingen te bekijken, of bij het bevestigen van het aantal verwijzingen te helpen die de staat van uw partners u verstrekt.

Deze pagina kan alleen correct worden ingevuld als aan verschillende vereisten is voldaan:
* Als het gebruiken van het handspoor van de douanekoppeling, moet een `tl()` verzoek met de middenparameter worden in brand gestoken die aan wordt geplaatst `e`.
* Als u automatische aangepaste koppelingencontrole gebruikt, moet aan alle vereisten worden voldaan:
   * De variabele [trackExternalLinks](/help/implement/vars/config-vars/trackexternallinks.md) moet zijn ingeschakeld.
   * De koppeling waarop de gebruiker heeft geklikt, mag niet overeenkomen met waarden binnen de variabele [linkInternalFilters](/help/implement/vars/config-vars/linkinternalfilters.md) .
   * Als de variabele [linkExternalFilters](/help/implement/vars/config-vars/linkexternalfilters.md) bestaat, moet de externe koppeling overeenkomen met ten minste een van de waarden die in deze variabele zijn ingesteld.
* Als aan een van de bovenstaande voorwaarden niet wordt voldaan, vult de treffer dit rapport niet in.
* Net als bij alle aangepaste resultaten voor het bijhouden van koppelingen, wordt de variabele [pageName](/help/implement/vars/page-vars/pagename.md) uit de afbeeldingsaanvraag verwijderd om te voorkomen dat de pagina wordt opgevuld met metrische informatie.
* U kunt dit rapport weergeven in een georiënteerde en gerangschikte indeling.
* Dit rapport kan een onderzoeksfilter gebruiken om van specifieke lijnpunten de plaats te bepalen.
* U kunt [onderverdelingen](/help/analyze/reports-analytics/reports-customize/breakdowns.md) maken met elke andere variabele.
