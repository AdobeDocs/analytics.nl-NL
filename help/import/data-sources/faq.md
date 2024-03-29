---
title: Veelgestelde vragen over gegevensbronnen
description: Veelgestelde vragen over gegevensbronnen.
exl-id: a948dfe9-289f-43e2-a9e7-7990cf609f5c
feature: Data Sources
role: Admin
source-git-commit: f7d07525c97f4aa145dc46198f883a37cde80158
workflow-type: tm+mt
source-wordcount: '400'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensbronnen

Veelgestelde vragen over gegevensbronnen.

+++Wat zijn de kosten om gegevensbronnen te gebruiken?
Gegevensbronnen maken geen kosten en tellen ook niet voor het gebruik van serveroproepen. [Volledige verwerkingsgegevensbronnen](full-processing-eol.md) geteld naar serveroproepen vóór hun pensionering.
+++

+++Hoe beïnvloeden gegevensbronnen attributie en vervaldatum voor eVars?
Als een transactieID tussen een gegevensbron en een online treffer aanpast, veronderstellen de bijbehorende waarden van eVar de zelfde attributie en de vervaldatum alsof zij op de online slag werden geplaatst.

Alle andere gegevens die via gegevensbronnen zijn geüpload, hebben geen kenmerk of vervaldatum.
+++

+++Hoe beïnvloeden de gegevensbronnen standaardmetriek, zoals paginameningen, bezoeken, of unieke bezoekers?
Gegevens die via gegevensbronnen zijn geüpload, hebben geen invloed op [Paginaweergaven](/help/components/metrics/page-views.md), [Bezoeken](/help/components/metrics/visits.md), of [Unieke bezoekers](/help/components/metrics/unique-visitors.md) op welke wijze dan ook. De enige standaardmetrisch die zij beïnvloeden omvat [Voorval](/help/components/metrics/occurrences.md).
+++

+++Kan ik gegevens verwijderen die met gegevensbronnen zijn geïmporteerd?

Ja. U kunt deze gegevens verwijderen met de [API voor gegevensherstel](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/data-repair/). Bovendien beveelt de Adobe ten zeerste aan gegevensbronnen te uploaden naar een testrapportsuite voordat deze in een productierapportsuite wordt geüpload.
+++

+++Hoeveel gegevens kan ik tegelijkertijd importeren?

De verwerking wordt gepauzeerd als de grootte groter is dan 50 MB en pas wordt hervat als het totaal kleiner is dan 50 MB. Zorg ervoor dat de totale grootte van alle bestanden op de FTP-site kleiner is dan 50 MB.
+++

+++Wat gebeurt als ik negatieve waarden in het melden door gegevensbronnen overga?

De waarde wordt dienovereenkomstig verlaagd. Sommige organisaties gebruiken negatieve gegevensbronwaarden om te proberen om gegevens te verbeteren. Negatieve gegevensbronwaarden kunnen rapporten op potentieel ongewenste of onverwachte manieren beïnvloeden. Adobe raadt aan alleen in laatste instantie negatieve gegevensbronnen te gebruiken.
+++

+++Zijn bestandsextensies hoofdlettergevoelig?
Ja. Bestanden met een extensie van `.TXT` of `.FIN` niet worden verwerkt. Zorg ervoor dat de bestandsextensies allemaal in kleine letters worden weergegeven.
+++

+++Hoeveel kolommen kan ik aan een gegevensbrondossier toevoegen?
U kunt zo veel kolommen aan een gegevensbrondossier omvatten aangezien u zou willen, als zij alle geldige kolommen zijn. Zie [Bestandsindeling](file-format.md) voor een lijst met geldige namen van variabelen en kolommen.
+++

+++Kan ik gegevensbronnen gebruiken zonder de door de Adobe verschafte FTP-locatie te gebruiken?
U kunt de [API voor gegevensbronnen](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), waarmee u API-aanroepen rechtstreeks naar de Adobe kunt verzenden. Deze API-aanroepen bevatten een `UploadData` methode, waarmee u gegevens kunt verzenden via een JSON-objectlading.
+++
