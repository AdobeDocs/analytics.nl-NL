---
title: Veelgestelde vragen over gegevensbronnen
description: Veelgestelde vragen over gegevensbronnen.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
role: Admin
source-git-commit: 667870f9575bbc03a72738771f34bf1718725d6c
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensbronnen

Veelgestelde vragen over gegevensbronnen.

+++Wat zijn de kosten om gegevensbronnen te gebruiken?
Gegevensbronnen maken geen kosten en tellen ook niet voor het gebruik van serveroproepen. [ Volledige bronnen van verwerkingsgegevens ](full-processing-eol.md) geteld naar servervraag vóór hun pensionering.
+++

+++Hoe beïnvloeden gegevensbronnen attributie en vervaldatum voor eVars?
Gegevensbronnen hebben geen attributie of vervaldatum.
+++

+++Hoe beïnvloeden gegevensbronnen metriek zoals paginameningen, bezoeken, of unieke bezoekers?
De gegevens die door gegevensbronnen worden geupload beïnvloeden [ meningen van de Pagina ](/help/components/metrics/page-views.md), [ bezoeken ](/help/components/metrics/visits.md), of [ Unieke bezoekers ](/help/components/metrics/unique-visitors.md) op geen enkele manier. Het enige gebrek metrisch dat zij beïnvloeden omvat [ Voorkomen ](/help/components/metrics/occurrences.md).
+++

+++Werken gegevens die via gegevensbronnen zijn geüpload door extra verwerking, zoals verwerkingsregels?
Nee. Gegevens geüpload via gegevensbronnen:

* Ga niet door [ Regels van de Verwerking ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/processing-rules/pr-overview.md)
* Ga niet door [ de verwerkingsregels van het Kanaal van de Marketing ](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/marketing-channels/c-rules.md)
* Ga niet door [ regels VISTA ](/help/technotes/vista.md)
+++

+++Kan ik gegevens verwijderen die met gegevensbronnen zijn geïmporteerd?
Ja. U kunt dit gegeven schrappen gebruikend [ Reparatie API van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/). Adobe raadt ten zeerste aan gegevensbronnen te uploaden naar een testrapportsuite voordat deze wordt geüpload naar een productierapportsuite om de noodzaak om gegevens te verwijderen te beperken.
+++

+++Hoeveel gegevens kan ik tegelijkertijd importeren?
De verwerking wordt gepauzeerd als de grootte groter is dan 50 MB en pas wordt hervat als het totaal kleiner is dan 50 MB. Zorg ervoor dat de totale grootte van alle bestanden op de FTP-site kleiner is dan 50 MB.
+++

+++Wat gebeurt er als ik negatieve waarden doorgeef in rapportage via gegevensbronnen?
De waarde wordt dienovereenkomstig verlaagd. Sommige organisaties gebruiken negatieve gegevensbronwaarden om te proberen om gegevens te verbeteren. Negatieve gegevensbronwaarden kunnen rapporten op potentieel ongewenste of onverwachte manieren beïnvloeden. Adobe raadt aan alleen in laatste instantie negatieve waarden in gegevensbronnen te gebruiken.
+++

+++Zijn bestandsextensies hoofdlettergevoelig?
Ja. Bestanden met de extensie `.TXT` of `.FIN` worden niet verwerkt. Zorg ervoor dat de bestandsextensies allemaal in kleine letters worden weergegeven.
+++

+++Hoeveel kolommen kan ik aan een gegevensbrondossier toevoegen?
U kunt zo veel kolommen aan een gegevensbrondossier omvatten aangezien u zou willen, als zij alle geldige kolommen zijn. Zie [ formaat van het Dossier ](file-format.md) voor een lijst van geldige variabele/kolomnamen.
+++

+++Kan ik gegevensbronnen gebruiken zonder de door Adobe verschafte FTP-locatie te gebruiken?
U kunt [ Gegevensbronnen API ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/) gebruiken, die u toestaat om API vraag rechtstreeks naar Adobe te verzenden. Deze API-aanroepen bevatten een methode `UploadData` , waarmee u gegevens kunt verzenden via een JSON-objectlading.
+++
