---
description: Hiermee geeft u een aantal overwegingen weer die u moet kennen voordat u segmenten verwijdert.
title: Segmenten verwijderen
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: 80e4a3ba4a5985563fcf02acf06997b4592261e4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Segmenten verwijderen

Dit artikel bevat een aantal overwegingen die u in acht moet nemen voordat u segmenten verwijdert.

Wanneer u een segment verwijdert:

* Geplande rapporten en dashboards die dit segment hebben toegepast blijven normaal werken. Het segment of dashboard gebruikt bijvoorbeeld nog steeds het verwijderde segment.
* Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier is een voorbeeld: veronderstel u 2 segmenten met de zelfde naam in verschillende rapportreeksen hebt:

  | Segmentnaam | Rapportsuite |
  |---|---|
  | Bezoeken vanuit Californië | mainprod |
  | Bezoeken vanuit Californië | maindev |

  U hebt een bladwijzer die naar het segment voor de [!UICONTROL mainprod] rapportreeks verwijst. Vervolgens verwijdert u dat segment omdat het segment een duplicaat is. De bladwijzer zal blijven lopen, verwijzend naar de definitie van het geschrapte segment. Als u de segmentdefinitie voor het resterende segment wijzigt en Catalina Island en Tijuana Mexico opneemt, verandert het segment dat op de bladwijzer is toegepast niet. Het segment zal de oude definitie gebruiken. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapt segment gebruikt, kon u de naam van het resterende segment veranderen om erop te wijzen of de referentie het resterende segment gebruikt.
