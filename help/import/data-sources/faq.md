---
title: Veelgestelde vragen over gegevensbronnen
description: Veelgestelde vragen over gegevensbronnen.
source-git-commit: bb3036380eeec9b7a868f60a4c9076f2b772532b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# Veelgestelde vragen over gegevensbronnen

Veelgestelde vragen over gegevensbronnen.

+++Wat zijn de kosten om gegevensbronnen te gebruiken?
Gegevensbronnen maken geen kosten en tellen ook niet voor het gebruik van serveroproepen. [Volledige verwerkingsgegevensbronnen](full-processing-eol.md) geteld naar serveroproepen vóór hun pensionering.
+++

+++Hoe beïnvloeden gegevensbronnen attributie en vervaldatum voor eVars?
Als een transactieID tussen een gegevensbron en een online hit aanpast, nemen de bijbehorende eVar de zelfde attributie en de vervaldatum aan alsof zij op de online slag werden geplaatst.

Alle andere gegevens die via gegevensbronnen zijn geüpload, hebben geen kenmerk of vervaldatum.
+++

+++Hoe beïnvloeden de gegevensbronnen standaardmetriek, zoals paginameningen, bezoeken, of unieke bezoekers?
Gegevens die via gegevensbronnen zijn geüpload, hebben geen invloed op [Paginaweergaven](/help/components/metrics/page-views.md), [Bezoeken](/help/components/metrics/visits.md), of [Unieke bezoekers](/help/components/metrics/unique-visitors.md) op welke wijze dan ook. De enige standaardmetrisch die zij beïnvloeden omvat [Voorval](/help/components/metrics/occurrences.md).
+++

+++Kan ik gegevens verwijderen die met gegevensbronnen zijn geïmporteerd?

**Nee.** Gegevens die met behulp van gegevensbronnen in rapporten zijn geüpload, zijn **permanent**. Het kan niet worden verwijderd, zelfs niet door Adobe, zodra het is geïmporteerd. Adobe raadt u ten zeerste aan gegevensbronnen te uploaden naar een testrapportsuite voordat u deze uploadt naar een productierapportsuite.
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

+++Kan ik gegevensbronnen gebruiken zonder de door Adobe verschafte FTP-locatie te gebruiken?
U kunt de [API voor gegevensbronnen](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-sources/), waarmee u API-aanroepen rechtstreeks naar Adobe kunt verzenden. Deze API-aanroepen bevatten een `UploadData` methode, waarmee u gegevens kunt verzenden via een JSON-objectlading.
+++
