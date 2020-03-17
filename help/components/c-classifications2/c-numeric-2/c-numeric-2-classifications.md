---
description: Numerieke 2 classificaties bieden aangepaste, flexibele maateenheden die u via de importer kunt importeren in de Adobe Experience Cloud.
subtopic: Classifications
title: Overzicht van numerieke 2 classificaties
topic: Admin tools
uuid: cbea7cd1-3a92-4e9d-b671-646e9add1ee6
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Overzicht van numerieke 2 classificaties

Numerieke 2 classificaties bieden aangepaste, flexibele maateenheden die u via de importer kunt importeren in de Adobe Experience Cloud.

>[!IMPORTANT]
>
>De mogelijkheid om classificaties met numerieke waarden 2 en datum in te voeren is uit de codebase verwijderd. Deze wijziging wordt van kracht met ingang van het onderhoudscontract van juli 2019. Als u Numerieke of Datum-Toegelaten kolommen in uw de invoerdossier hebt, zullen die cellen stil worden genegeerd, en om het even welke andere gegevens binnen dat dossier zullen worden ingevoerd als normaal. Bestaande classificaties kunnen nog steeds worden geëxporteerd via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage.

> [!NOTE] In de versie Analytics Maintenance van 10 mei 2018, heeft Adobe de functionaliteit van voor datums geschikte en numerieke classificaties beperkt. Deze classificatietypen zijn verwijderd uit de interfaces Admin en Classification Importer. Er kunnen geen nieuwe datums en numerieke classificaties worden toegevoegd. Bestaande classificaties kunnen nog steeds worden beheerd (geüpload naar, verwijderd) via de standaardclassificatieworkflow en blijven beschikbaar in de rapportage.

Een gebruikelijke manier om numerieke 2 classificaties te gebruiken is voor numerieke variabelen die in de loop der tijd veranderen voor verschillende items, zoals de kostprijs van verkochte goederen. In admin kunt u classificaties op de [!UICONTROL Conversion Classification] pagina maken en vervolgens de importer gebruiken om een bestand te exporteren, bewerkingen uit te voeren en het bestand vervolgens weer in Adobe te importeren. Na het invoeren van de gegevens, kunt u de numerieke classificaties gebruiken wanneer het creëren van berekende metriek.

>[!IMPORTANT]
>
>De Werkruimte van de analyse en de Ad hoc Analyse steunen geen Numeric 2 classificaties.

In de volgende tabel worden de verschillen tussen de classificatietypen weergegeven:

| FUNCTIE | TEXT | NUMERIEK 1.0 | NUMERIC 2.0 |
|---|---|---|---|
| Weergeven als een rapport | Ja | Nee | Nee |
| Kan als metrisch worden gebruikt | Nee | Ja | Ja |
| Kan worden gemaakt op basis van het basisrapport | Ja | Nee | Ja |
| Berekend op basis van gebeurtenissen | Nee | Ja | Ja |
| Meerdere rijen per sleutel | Nee | Nee | Ja |
| Kan verschillende waarden hebben voor verschillende tijdsperiodes | Nee | Nee | Ja |
| Kan worden gebruikt in berekende metriek | Nee | Ja | Ja |

