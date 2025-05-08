---
title: Classificatiegegevens exporteren via FTP
description: De uitvoer van FTP verstrekt meer flexibiliteit met gegevenssetdownloads, met inbegrip van het downloaden van gegevens van veelvoudige rapportreeksen en het downloaden van gegevenssetdossiers groter dan 50.000 gegevensrijen
feature: Classifications
exl-id: 6f97f0b2-1a04-407f-9df9-8715da52037d
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '590'
ht-degree: 0%

---

# FTP-export (verouderd)

De optie FTP biedt meer flexibiliteit bij het downloaden van gegevenssets, zoals de mogelijkheid om gegevens te downloaden uit meerdere rapportsuite en bestanden van gegevenssets te downloaden die groter zijn dan 50.000 gegevensrijen. Maak een FTP-account voordat u classificatiegegevens downloadt via FTP.

Houd rekening met het volgende wanneer u gegevensfilters toepast:

* U kunt jokertekens gebruiken bij het definiëren van het gegevensfilter. Gebruik een sterretje `*` om nul of meer tekens en een vraagteken `?` af te stemmen op precies één teken. Gebruik `?*` om een of meer tekens overeen te laten komen.
* Wanneer u beide typen gegevensfilters toepast op een download, worden doorgaans alleen rijen gedownload die aan beide regels voldoen. De volgende uitzonderingen zijn echter van toepassing:
   * Als Rijen met lege kolom = Alle Kolommen, dan worden alle kolommen behalve de kolom die in de eerste regel wordt gespecificeerd gecontroleerd leegte. Deze uitzondering zorgt ervoor dat het hulpmiddel om het even welke rij met een kolom downloadt die de eerste regel aanpast die ook alle andere lege kolommen heeft.
   * Wanneer het downloaden van gegevensrijen die op lege kolommen worden gebaseerd, worden alle kolommen behalve die gespecificeerd in de eerste regel gecontroleerd leegte.
   * Als dezelfde kolom voor beide filterregels is opgegeven (het is bijna onmogelijk om aan beide criteria te voldoen), worden alleen rijen gedownload die aan de eerste regel voldoen.
   * Voor FTP-export geldt een limiet van 30 kolommen.

## Classificaties exporteren met FTP

In deze stappen wordt beschreven hoe u classificaties vanuit Adobe Analytics exporteert (downloadt) met behulp van FTP.

1. Maak een FTP-account.
1. Ga naar [!UICONTROL Admin] > [!UICONTROL Classification Importer] .
1. Klik op de tab **[!UICONTROL FTP Import]** .
1. Configureer velden voor de FTP-export.
1. Klik op **[!UICONTROL Export File]**.
1. Sla de gegevensset op uw lokale systeem op.

## Veldomschrijvingen

| Element | Beschrijvingen |
| --- | --- |
| [!UICONTROL Select Report Suite] | Selecteer de rapportsuite waaruit u de rapportgegevens wilt exporteren. |
| [!UICONTROL Data Set to be classified] | Selecteer in het keuzemenu de gegevensset die u wilt classificeren. |
| [!UICONTROL Select Number of Rows] | Geef op hoeveel rijen met gegevens u wilt exporteren.<ul><li>Selecteer **[!UICONTROL All]** om alle rapportgegevens te downloaden.</li><li>Selecteer **[!UICONTROL Limit Data Rows To]** als u een specifiek aantal rijen wilt opgeven dat u wilt downloaden.</li></ul> |
| [!UICONTROL Filter by Date Received] | (Optioneel) Filter de gegevens op de datum waarop ze zijn ontvangen. Geef het datumbereik op waarvoor u gegevens wilt downloaden. |
| [!UICONTROL Apply Data Filter] | (Optioneel) Filter de gegevensset op basis van gegevenscriteria. U kunt de download filteren en gegevensrijen met een bepaalde waarde of gegevensrijen met niet-toegewezen kolomwaarden (classificatie) opnemen. |
| [!UICONTROL Date Filter] | (Optioneel) Gegevens filteren op campagnegegevens. U kunt gegevens alleen downloaden uit actieve campagnes of campagnes selecteren die in een specifiek datumbereik beginnen (of eindigen). |
| [!UICONTROL Export Numeric 2] | U kunt numerieke 2 classificaties in het systeem importeren met behulp van de importer. Numerieke 2 classificaties zijn nuttig voor variabelen die in tijd veranderen voor verschillende punten, zoals kosten en begrotingswaarden voor het rapport van het Kanaal van de Marketing. |
| [!UICONTROL FTP Account] | Geef de FTP-serverinformatie op waar Adobe het gegevensbestand moet downloaden, zoals de hostnaam en -poort, het pad naar de doelmap, de gebruikersnaam en het wachtwoord. |
| [!UICONTROL Notification] | Geef het e-mailadres op waar meldingen over deze FTP-download moeten worden ontvangen. |
| [!UICONTROL Encoding] | Selecteer de tekencodering voor het gegevensbestand. De standaardcoderingsindeling is UTF-8 of ISO-8859-1, op basis van de codering die voor de classificatie is geüpload. UTF-8 in UTF-16 zet uw UTF-8 gecodeerde classificaties in UTF-16 het coderen om. ISO-8859-1 in UTF-16 zet uw ISO-8859-1 gecodeerde classificaties in UTF-16 het coderen om.<br>**Nota:** als u om in UTF-16 selecteert om te zetten, moet bron het coderen de codering van origineel aanpassen uploadt of u kunt onverwachte resultaten krijgen. We raden u aan alle geüploade bestanden zonder BOM te coderen in UTF-8. |
