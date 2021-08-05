---
title: Browser exporteren
description: Met exporteren vanuit de browser kunt u uw classificatiegegevens exporteren naar een door tabs gescheiden bestand.
source-git-commit: 8a5c7309b5d4061b2e3241219d9bdb1521294535
workflow-type: tm+mt
source-wordcount: '404'
ht-degree: 0%

---


# Browser exporteren

Met exporteren vanuit de browser kunt u uw classificatiegegevens exporteren naar een door tabs gescheiden bestand.

Admin > Classification Importer

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

