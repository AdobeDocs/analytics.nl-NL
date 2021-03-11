---
description: 'Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer. U moet '
keywords: Gegevensfeed;aanbevolen methoden;verkeersstroom;uur;ftp
title: Beste praktijken en Algemene Informatie
uuid: f2d6c13a-5d4e-4fc2-8baa-28c69f0cf5f6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---


# Aanbevolen werkwijzen

Hieronder vindt u een aantal aanbevolen procedures voor de verwerking en levering van gegevensinvoer.

* Zorg ervoor dat u om het even welke verwachte verkeerspikes voortijdig overbrengt. Latentie heeft rechtstreeks invloed op de verwerkingstijd voor gegevensfeeds. Zie [Plan een verkeerspiek](/help/admin/c-traffic-management/t-traffic-schedule-spike.md) in de Admin gebruikershandleiding.
* Gegevensfeeds bevatten geen service-level overeenkomst, tenzij expliciet vermeld in uw contract met Adobe. Diervoeders worden meestal binnen enkele uren na het passeren van het rapportagevenster geleverd, maar kunnen soms wel 12 uur of meer in beslag nemen.
* Zorg ervoor dat er voldoende ruimte beschikbaar is op uw FTP-site. Verwijder regelmatig bestanden van het doel, zodat u niet per ongeluk te weinig schijfruimte hebt.
* Uurfeeds waarbij gebruik wordt gemaakt van meerdere leveringprocessen, het snelst. U kunt overwegen meerdere bestandsfeeds per uur te gebruiken als een tijdige levering een hoge prioriteit voor uw organisatie is.
* Als u sFTP gebruikt, moet u geen bestanden lezen of verwijderen met het achtervoegsel `.part`. Het achtervoegsel `.part` geeft aan dat het bestand gedeeltelijk wordt overgedragen. Nadat het bestand is overgebracht, verdwijnt het achtervoegsel `.part`.
* Als u het inslikken van de voeding automatiseert, moet u rekening houden met de mogelijkheid dat een bestand meerdere keren kan worden overgebracht. Dubbele bestanden kunnen opnieuw worden verzonden door de gebruiker of zelden door Adobe.
