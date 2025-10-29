---
title: Veelgestelde vragen over gegevensbronnen
description: Veelgestelde vragen over gegevensbronnen.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
role: Admin
source-git-commit: e934de3938f013067d6bbd6b516b0444b0c9f782
workflow-type: tm+mt
source-wordcount: '408'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensbronnen

Veelgestelde vragen over gegevensbronnen.

+++Wat zijn de kosten om gegevensbronnen te gebruiken?
Gegevensbronnen maken geen kosten en tellen ook niet voor het gebruik van serveroproepen. [&#x200B; Volledige bronnen van verwerkingsgegevens &#x200B;](full-processing-eol.md) geteld naar servervraag vóór hun pensionering.
+++

+++Hoe beïnvloeden gegevensbronnen attributie en vervaldatum voor eVars?
Gegevensbronnen hebben geen attributie of vervaldatum.
+++

+++Hoe beïnvloeden gegevensbronnen metriek zoals paginameningen, bezoeken, of unieke bezoekers?
De gegevens die door gegevensbronnen worden geupload beïnvloeden [&#x200B; meningen van de Pagina &#x200B;](/help/components/metrics/page-views.md), [&#x200B; bezoeken &#x200B;](/help/components/metrics/visits.md), of [&#x200B; Unieke bezoekers &#x200B;](/help/components/metrics/unique-visitors.md) op geen enkele manier. Het enige gebrek metrisch dat zij beïnvloeden omvat [&#x200B; Voorkomen &#x200B;](/help/components/metrics/occurrences.md).
+++

+++Werken gegevens die via gegevensbronnen zijn geüpload door extra verwerking, zoals verwerkingsregels?
Nee. Gegevens geüpload via gegevensbronnen:

* Ga niet door [&#x200B; Regels van de Verwerking &#x200B;](/help/admin/tools/manage-rs/edit-settings/general/processing-rules/pr-overview.md)
* Ga niet door [&#x200B; de verwerkingsregels van het Kanaal van de Marketing &#x200B;](/help/admin/tools/manage-rs/edit-settings/marketing-channels/mc-proc-rules.md)
* Ga niet door [&#x200B; regels VISTA &#x200B;](/help/technotes/vista.md)
+++

+++Kan ik gegevens verwijderen die met gegevensbronnen zijn geïmporteerd?
Ja. U kunt dit gegeven schrappen gebruikend [&#x200B; Reparatie API van Gegevens &#x200B;](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/). Adobe raadt ten zeerste aan gegevensbronnen te uploaden naar een testrapportsuite voordat deze wordt geüpload naar een productierapportsuite om de noodzaak om gegevens te verwijderen te beperken.
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
U kunt zo veel kolommen aan een gegevensbrondossier omvatten aangezien u zou willen, als zij alle geldige kolommen zijn. Zie [&#x200B; formaat van het Dossier &#x200B;](file-format.md) voor een lijst van geldige variabele/kolomnamen.
+++

+++Kan ik gegevensbronnen gebruiken zonder de door Adobe verschafte FTP-locatie te gebruiken?
U kunt [&#x200B; Gegevensbronnen API &#x200B;](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/) gebruiken, die u toestaat om API vraag rechtstreeks naar Adobe te verzenden. Deze API-aanroepen bevatten een methode `UploadData` , waarmee u gegevens kunt verzenden via een JSON-objectlading.
+++
