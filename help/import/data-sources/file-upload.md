---
title: Gegevensbronbestand uploaden naar Adobe
description: Het uploaden van een gegevensbronbestand naar Adobe Analytics voor opname.
exl-id: 64e3cd70-b511-4c4e-abd0-94eb36bc3519
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Gegevensbronbestand uploaden naar Adobe

Als u een gegevensbronbestand naar de Adobe verzendt, maakt dat deel uit van een standaard geverifieerde FTP-workflow. U kunt Windows Verkenner, de Vinder, of een specifieke cliënt van FTP gebruiken om de gewenste dossiers aan de plaats van FTP van de Adobe te uploaden.

Zoek de FTP-referenties in het dialoogvenster [Gegevensbronbeheer](manage.md). Elke gegevensbron heeft een koppeling naar zijn **[!UICONTROL FTP Info]**. Elke FTP-locatie wordt toegewezen aan die specifieke gegevensbron. U kunt niet dezelfde FTP-locatie gebruiken voor meerdere gegevensbronnen.

Om veiligheidsredenen zijn FTP-locaties zonder enige activiteit gedurende meer dan 30 dagen uitgeschakeld.

## De `.fin` file

Een essentieel onderdeel van het opnemen van een gegevensbronbestand is het opnemen van een `.fin` bestand. Dit bestand geeft aan dat het gegevensbestand gereed is voor verwerking. Als u een bestand met gegevensbronnen uploadt zonder bijbehorende `.fin` , verwerkt Adobe die gegevens nooit.

De `.fin` bestand heeft de volgende eigenschappen:

* Het bestand bevat een `.fin` extensie. Zorg ervoor dat het besturingssysteem het mogelijk maakt bestandstypen te bekijken en te bewerken.
* Het bestand is leeg. Gegevens niet opslaan in het dialoogvenster `.fin` bestand.
* Het bestand heeft exact dezelfde naam als het gegevensbronbestand. Als u bijvoorbeeld een gegevensbronbestand met de naam `example.txt`de `.fin` file **moet** worden benoemd `example.fin`. Als zij niet identiek worden genoemd, verwerkt de Adobe nooit het dossier van gegevensbronnen.

Wanneer zowel het gegevensbronbestand als `.fin` worden geüpload naar de FTP-site, verwerkt de Adobe het bestand. Upload de `.fin` bestand tot het gegevensbronbestand volledig is geüpload. Als de `.fin` Het bestand wordt voortijdig geüpload, het gedeeltelijk geüploade bestand wordt door de Adobe opgehaald en opgenomen, waardoor mogelijke fouten optreden.

## Verwerkingsopdracht

Als u meerdere bestanden tegelijk uploadt naar de FTP-site, worden deze door de Adobe in alfanumerieke volgorde opgenomen. Als uw organisatie vereist dat bestanden in een bepaalde volgorde worden opgenomen, moet u ervoor zorgen dat de bestandsnamen alfanumeriek worden genoemd.

## Verwerkingstijd

Om ervoor te zorgen dat bestanden zo snel mogelijk worden verwerkt, raadt de Adobe aan metrische gegevens samen te voegen tot één rij per datum. Dit gegevensbronbestand is bijvoorbeeld geldig, maar wordt langzamer verwerkt:

| `date` | `eVar1` | `event1` | `event2` | `event3` |
| --- | --- | --- | --- | --- |
| `07/24/YYYY` | `red` | `1` | | |
| `07/24/YYYY` | `red` | `1` | | |
| `07/24/YYYY` | `red` | | `1` | |
| `07/24/YYYY` | `red` | | | `1` |

Dit bestand wordt sneller verwerkt en bevat dezelfde gegevens:

| `date` | `eVar1` | `event1` | `event2` | `event3` |
| --- | --- | --- | --- | --- |
| `07/24/YYYY` | `red` | `2` | `1` | `1` |
