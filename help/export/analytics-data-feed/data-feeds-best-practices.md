---
description: 'Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer. U moet '
keywords: Data Feed;best practices;traffic spike;hourly;ftp
title: Beste praktijken en Algemene Informatie
uuid: f2d6c13a-5d4e-4fc2-8baa-28c69f0cf5f6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Aanbevolen werkwijzen

Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer.

* Zorg ervoor dat u om het even welke verwachte verkeerspikes voortijdig overbrengt. Latentie heeft rechtstreeks invloed op de verwerkingstijd voor gegevensfeeds. Zie [Een verkeerspiek](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) plannen in de gebruikershandleiding Admin.
* Gegevensfeeds bevatten geen overeenkomst op serviceniveau, tenzij dit expliciet wordt vermeld in uw contract met Adobe. Diervoeders worden meestal binnen enkele uren na het passeren van het rapportagevenster geleverd, maar kunnen soms wel 12 uur of meer in beslag nemen.
* Zorg ervoor dat er voldoende ruimte beschikbaar is op uw FTP-site. Verwijder regelmatig bestanden van het doel, zodat u niet per ongeluk te weinig schijfruimte hebt.
* Uurfeeds waarbij gebruik wordt gemaakt van meerdere leveringprocessen, het snelst. U kunt overwegen meerdere bestandsfeeds per uur te gebruiken als een tijdige levering een hoge prioriteit voor uw organisatie is.
* Als u sFTP gebruikt, kunt u geen bestanden met het `.part` achtervoegsel lezen of verwijderen. Het `.part` achtervoegsel geeft aan dat het bestand gedeeltelijk wordt overgedragen. Nadat het bestand is overgebracht, verdwijnt het `.part` achtervoegsel.
* Als u het inslikken van de voeding automatiseert, moet u rekening houden met de mogelijkheid dat een bestand meerdere keren kan worden overgebracht. Dubbele bestanden kunnen opnieuw worden verzonden door de gebruiker of zelden door Adobe.
