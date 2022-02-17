---
description: Hiermee geeft u een aantal overwegingen weer die u moet kennen voordat u segmenten verwijdert.
title: Segmenten verwijderen
feature: Segmentation
exl-id: 434b6fec-1dfa-4375-a9de-d47fad2c64bc
source-git-commit: 7a47d837eeae65f2e98123aca78029bfeb7ffe9d
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 1%

---

# Segmenten verwijderen

Hiermee geeft u een aantal overwegingen weer die u moet kennen voordat u segmenten verwijdert.

Wanneer u een segment verwijdert,

* Geplande rapporten en dashboards die dit segment hebben toegepast blijven normaal werken, d.w.z. het segment of dashboard blijft het verwijderde segment gebruiken.
* Geplande rapporten worden niet bijgewerkt wanneer u een segment met dezelfde naam bewerkt. Hier volgt een voorbeeld: Stel dat u twee segmenten met dezelfde naam in verschillende rapportsuites hebt:

   ![](assets/duplicate_seg_names.png)

   U hebt een referentie die naar het segment voor de belangrijkste rapportreeks verwijst. Dan schrapt u dat segment omdat het een duplicaat is. De bladwijzer blijft lopen, verwijzend naar de definitie van het geschrapte segment. Als u de segmentdefinitie voor het resterende segment wijzigt en Catalina Island en Tijuana Mexico opneemt, verandert het segment dat op de bladwijzer is toegepast niet. De oude definitie wordt gebruikt. Als u dit wilt corrigeren, werkt u de bladwijzer bij en verwijst u naar de nieuwe definitie. Als u niet zeker bent of een referentie, dashboard of gepland rapport een geschrapt segment gebruikt, kon u de naam van het resterende segment veranderen zodat is het duidelijker of de referentie het resterende segment gebruikt.
