---
title: Browser exporteren
description: Met exporteren vanuit de browser kunt u uw classificatiegegevens exporteren naar een door tabs gescheiden bestand.
source-git-commit: d522303de5beb6a10d95ad2da523774ea595ae2d
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---


# Browser exporteren

Met exporteren vanuit de browser kunt u uw classificatiegegevens exporteren naar een door tabs gescheiden bestand.

[!UICONTROL Admin] > [!UICONTROL Classification Importer]

Het gegevenssetbestand is een door tabs gescheiden gegevensbestand (bestandsnaamextensie .tab) dat door de meeste spreadsheettoepassingen wordt ondersteund.

>[!NOTE]
>Voor het exporteren van browsers geldt een limiet van 30 kolommen.

## Veldomschrijvingen

| Element | Beschrijvingen |
| --- | --- |
| Rapportsuite selecteren | Selecteer de rapportsuite waaruit u de rapportgegevens wilt exporteren. |
| Te classificeren gegevensset | Selecteer in het keuzemenu de gegevensset die u wilt classificeren. |
| Aantal rijen selecteren | Geef op hoeveel rijen met gegevens u wilt exporteren.<ul><li>Selecteer **[!UICONTROL All]** om alle rapportgegevens (maximaal 50.000 rijen) te downloaden.</li><li>Selecteer **[!UICONTROL Limit Data Rows To]** als u een specifiek aantal rijen wilt specificeren om te downloaden.</li></ul>Als u meer dan 50.000 gegevensrijen wilt downloaden, gebruikt u de FTP-downloadoptie. |
| Filteren op datum ontvangen | (Optioneel) Filter de gegevens op de datum van ontvangst. Geef het datumbereik op waarvoor u gegevens wilt downloaden. |
| Gegevensfilter toepassen | (Optioneel) Filter de gegevensset op basis van gegevenscriteria. U kunt de download filteren en gegevensrijen met een bepaalde waarde of gegevensrijen met niet-toegewezen kolomwaarden (classificatie) opnemen. Houd rekening met het volgende wanneer u gegevensfilters toepast:<ul><li>U kunt jokertekens gebruiken bij het definiëren van het gegevensfilter. Gebruik een asterisk om nul of meer karakters en een vraagteken `?` aan precies één karakter aan te passen. Gebruik `?*` om één of meerdere karakters aan te passen.</li><li>Wanneer u beide typen gegevensfilters toepast op een download, worden doorgaans alleen rijen gedownload die aan beide regels voldoen. De volgende uitzonderingen zijn echter van toepassing:<ul><li>Als Rijen met lege kolom = Alle Kolommen, dan worden alle kolommen behalve de kolom die in de eerste regel wordt gespecificeerd gecontroleerd leegte. Deze uitzondering zorgt ervoor dat het systeem om het even welke rij met een kolom downloadt die de eerste regel aanpast die ook alle andere kolommen leeg heeft.</li><li>Wanneer het downloaden van gegevensrijen die op lege kolommen worden gebaseerd, worden alle kolommen behalve die gespecificeerd in de eerste regel gecontroleerd leegte.</li><li>Als dezelfde kolom voor beide filterregels is opgegeven (het is bijna onmogelijk om aan beide criteria te voldoen), worden alleen rijen gedownload die aan de eerste regel voldoen.</li></ul></ul> |
| Gegevensfilter | (Optioneel) Filter gegevens op campagnegegevens. U kunt gegevens alleen downloaden van actieve campagnes of u kunt campagnes selecteren die zijn gestart (of beëindigd) in een specifiek datumbereik.<br>**Belangrijk**: Deze optie is niet beschikbaar voor rapportsuites die zijn ingeschakeld voor de nieuwe classificatiearchitectuur. |
| Numeriek 2 exporteren | U kunt numerieke 2 classificaties in het systeem importeren met behulp van de importer. Numerieke 2 classificaties zijn nuttig voor variabelen die in tijd veranderen voor verschillende punten, zoals kosten en begrotingswaarden voor het rapport van het Kanaal van de Marketing. Zie Numerieke 2 classificaties voor informatie over het uploaden van gegevens met numerieke 2 classificaties. |
| Codering | Selecteer de tekencodering voor het gegevensbestand. De standaardcoderingsindeling is UTF-8 of ISO-8859-1, op basis van de codering die voor de classificatie is geüpload. UTF-8 in UTF-16 zet uw UTF-8 gecodeerde classificaties in UTF-16 het coderen om. ISO-8859-1 in UTF-16 zet uw ISO-8859-1 gecodeerde classificaties in UTF-16 het coderen om.<br>**Opmerking:** Als u ervoor kiest om om te zetten in UTF-16, moet de broncodering overeenkomen met de codering van de oorspronkelijke upload, anders krijgt u mogelijk onverwachte resultaten. We raden u aan alle geüploade bestanden zonder BOM te coderen in UTF-8. |
| Uitvoer prijsopgave | Geeft versie 2.1 op voor het classificatiebestand. Met deze instelling plaatst u aanhalingstekens rond speciale tekens om ervoor te zorgen dat de exportbewerking in Excel werkt wanneer een regeleinde bestaat in de waarden van de eVar. U kunt zien of een classificatiebestand versie 2.1 is door het gedownloade bestand te openen. U ziet v2.1 in de koptekst. Bijvoorbeeld: `## SC SiteCatalyst SAINT Import File v:2.1` |

## Classificatiegegevens exporteren met de browser

1. Klik op [!UICONTROL Admin] > [!UICONTROL Classification Importer].
1. Klik op het tabblad [!UICONTROL Browser Export].
1. Geef de gegevens van de gegevensset op.
1. Klik op [!UICONTROL Export File].
1. Sla de gegevensset op uw lokale systeem op.
