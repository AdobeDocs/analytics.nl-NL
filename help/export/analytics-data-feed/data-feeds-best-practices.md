---
description: Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer.
keywords: Gegevensfeed;aanbevolen methoden;verkeersstroom;uur;ftp
title: Beste praktijken en Algemene Informatie
feature: Data Feeds
exl-id: 5f6fbc13-b176-4f69-8f2d-7accc6e6ac2d
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Aanbevolen werkwijzen

Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer.

* Zorg ervoor dat u om het even welke verwachte verkeerspikes voortijdig overbrengt. Latentie heeft rechtstreeks invloed op de verwerkingstijd voor gegevensfeeds. Zie [Plan een verkeerspiek](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) in de handleiding voor Admin-gebruikers.

* Gegevensfeeds bevatten geen service-level overeenkomst, tenzij expliciet vermeld in uw contract met Adobe. Diervoeders worden meestal binnen enkele uren na het passeren van het rapportagevenster geleverd, maar kunnen soms wel 12 uur of meer in beslag nemen.

* Zorg ervoor dat er voldoende ruimte beschikbaar is op uw FTP-site. Verwijder regelmatig bestanden van het doel, zodat u niet per ongeluk te weinig schijfruimte hebt.

* Uurfeeds waarbij gebruik wordt gemaakt van meerdere aanleverprocessen, het snelst. U kunt overwegen meerdere bestandsfeeds per uur te gebruiken als een tijdige levering een hoge prioriteit voor uw organisatie is.

* Als u sFTP gebruikt, moet u bestanden niet lezen of verwijderen met een `.part` achtervoegsel. De `.part` Het achtervoegsel geeft aan dat het bestand gedeeltelijk wordt overgedragen. Als het bestand eenmaal is overgedragen, wordt het `.part` het achtervoegsel verdwijnt.

* Als u het inslikken van een feed automatiseert, moet u rekening houden met de mogelijkheid dat hits en bestanden meerdere keren kunnen worden overgebracht. Tijdens het innemen van de feed moeten dubbele treffers en dubbele bestanden worden afgehandeld zonder dat gegevens worden verwijderd of gedupliceerd. We raden u aan de combinatie van de `hitid_high` en `hitid_low` kolommen om een treffer uniek te identificeren.

   In zeldzame gevallen kunt u dubbel zien `hitid_high` en `hitid_low` waarden. Als dit gebeurt, bevestigt u dat het bestand niet eerder is verzonden en verwerkt. Als slechts enkele rijen in een bestand zijn gedupliceerd, kunt u het volgende toevoegen `visit_num` en `visit_page_num` om de uniciteit te helpen bepalen.
