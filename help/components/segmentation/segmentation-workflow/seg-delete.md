---
description: Hiermee geeft u een aantal overwegingen weer die u moet kennen voordat u segmenten verwijdert.
title: Segmenten verwijderen
topic: Segments
uuid: cb6db6ad-f400-4633-900a-8a02dcfccf2c
translation-type: tm+mt
source-git-commit: 9e70cd51f8828cdcb698175a2b4c0150610d14d0
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 5%

---


# Segmenten verwijderen

Hiermee geeft u een aantal overwegingen weer die u moet kennen voordat u segmenten verwijdert.

Wanneer u een segment verwijdert,

* Geplande rapporten en dashboards die dit segment hebben toegepast blijven normaal werken, d.w.z. het segment of dashboard blijft het verwijderde segment gebruiken.
* Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier volgt een voorbeeld: Stel dat u twee segmenten met dezelfde naam in verschillende rapportsuites hebt:

   ![](assets/duplicate_seg_names.png)

   U hebt een referentie die naar het segment voor de belangrijkste rapportreeks verwijst. Dan schrapt u dat segment omdat het een duplicaat is. De bladwijzer blijft lopen, verwijzend naar de definitie van het geschrapte segment. Als u de segmentdefinitie voor het resterende segment wijzigt en Catalina Island en Tijuana Mexico opneemt, verandert het segment dat op de bladwijzer is toegepast niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapt segment gebruikt, kon u de naam van het resterende segment veranderen zodat is het duidelijker of de referentie het resterende segment gebruikt.

## Ingesloten verwijderde segmenten bewerken in Ad Hoc Analysis {#section_976D601DBD2244E38B0A0222E31D2610}

In Ad Hoc Analysis kunt u nu ingesloten verwijderde segmenten bewerken in de [Berekende metrische bouwer](https://docs.adobe.com/content/help/nl-NL/analytics/components/calculated-metrics/cm-overview.html) en kunt u de bewerking &quot;Opslaan als&quot; op dat segment uitvoeren.

Alle andere verwijderde segmenten die naar het verwijderde segment verwijzen, blijven echter ongewijzigd.
