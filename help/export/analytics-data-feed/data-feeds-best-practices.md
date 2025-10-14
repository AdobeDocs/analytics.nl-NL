---
description: Meer informatie over de beste werkwijzen voor het verwerken en leveren van gegevensinvoer in Analytics.
keywords: Gegevensfeed;aanbevolen methoden;verkeersstroom;uur;ftp
title: Beste praktijken en Algemene Informatie
feature: Data Feeds
exl-id: 5f6fbc13-b176-4f69-8f2d-7accc6e6ac2d
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# Aanbevolen werkwijzen voor gegevensfeeds

Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer.

* Zorg ervoor dat u om het even welke verwachte verkeerspikes voortijdig overbrengt. Latentie heeft rechtstreeks invloed op de verwerkingstijd voor gegevensfeeds. Zie [&#x200B; Plan een verkeerspiek &#x200B;](/help/admin/tools/manage-rs/edit-settings/c-traffic-management/t-traffic-schedule-spike.md) in de Admin gebruikersgids.

* Gegevensfeeds bevatten geen service-level overeenkomst, tenzij expliciet vermeld in uw contract met Adobe. Diervoeders worden meestal binnen enkele uren na het passeren van het rapportagevenster geleverd, maar kunnen soms wel 12 uur of meer in beslag nemen.

* Uurfeeds waarbij gebruik wordt gemaakt van meerdere leveringprocessen, het snelst. U kunt overwegen meerdere bestandsfeeds per uur te gebruiken als een tijdige levering een hoge prioriteit voor uw organisatie is.

* Als u het inslikken van een feed automatiseert, moet u rekening houden met de mogelijkheid dat hits en bestanden meerdere keren kunnen worden overgebracht. Tijdens het innemen van de feed moeten dubbele treffers en dubbele bestanden worden afgehandeld zonder dat gegevens worden verwijderd of gedupliceerd. We raden u aan de combinatie van de kolommen `hitid_high` en `hitid_low` te gebruiken om een treffer op unieke wijze te identificeren.

  In zeldzame gevallen ziet u mogelijk dubbele `hitid_high` - en `hitid_low` -waarden. Als dit gebeurt, bevestigt u dat het bestand niet eerder is verzonden en verwerkt. Als slechts enkele rijen in een bestand gedupliceerd zijn, kunt u `visit_num` en `visit_page_num` toevoegen om de uniciteit te bepalen.

* Als het gebruiken van FTP (niet geadviseerd) zorg ervoor dat u ruime ruimte op uw plaats van FTP hebt. Verwijder regelmatig bestanden van het doel, zodat u niet per ongeluk te weinig schijfruimte hebt.

* Als u sFTP gebruikt (niet aanbevolen), kunt u geen bestanden met het achtervoegsel `.part` lezen of verwijderen. Het achtervoegsel `.part` geeft aan dat het bestand gedeeltelijk wordt overgedragen. Nadat het bestand is overgebracht, verdwijnt het achtervoegsel `.part` .