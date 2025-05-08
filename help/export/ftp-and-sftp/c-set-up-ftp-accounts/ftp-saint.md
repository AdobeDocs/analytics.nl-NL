---
description: De FTP-optie voor classificaties (SAINT) biedt meer flexibiliteit bij het uploaden van grote sets classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en om gegevenssets te uploaden die groter zijn dan 50.000 rijen.
keywords: ftp;sftp
title: Classificaties
feature: FTP Export
exl-id: fc783328-a70b-4af3-b3d3-c59ab79d6b8f
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---

# Classificaties

De FTP-optie voor classificaties biedt meer flexibiliteit bij het uploaden van grote sets met classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en gegevenssets te uploaden die groter zijn dan 50.000 rijen.

De tijd die het systeem nodig heeft om deze bestanden te importeren, varieert op basis van een aantal factoren. Als een geüpload bestand meer dan drie dagen op de FTP-server aanwezig is, kunt u contact opnemen met de door uw organisatie ondersteunde gebruikers om contact op te nemen met de klantenservice van Adobe.

Wanneer het importeren is gelukt, worden direct de juiste wijzigingen in een exportbewerking weergegeven, terwijl het wijzigen van de gegevens in Analytics maximaal vier uur kan duren bij het importeren van een browser en maximaal 24 uur bij het importeren van een FTP-bestand.

Voor informatie over de grenzen van FTP en gegevensbehoud, zie {de Limieten van FTP van 0} en het Behouden van Gegevens ](/help/export/ftp-and-sftp/ftp-limits.md).[

## Over het bestand `.fin` voor classificaties en gegevensbronnen uploaden {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een Classificatie- of Data Source-bestand (`.tab` of `.txt` ) uploadt, moet u voor het uploaden ook een leeg bestand uploaden met dezelfde naam als het gegevensbestand dat wordt geïmporteerd, maar met een .`.fin` extensie. Dit `.fin` -bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. Met het bestand `.fin` kan Adobe controleren of u klaar bent met importeren.

Nadat u zowel het bronbestand als het `.fin` -bestand hebt verzonden, is het belangrijk dat u zich afmeldt bij de FTP-site. De reden hiervoor is dat Adobe Analytics logout-gebeurtenissen gebruikt als een trigger waarmee bestanden kunnen worden verwerkt. Nadat het importeren is voltooid, verwijdert Adobe beide bestanden van de FTP-locatie.

Bestand voltooien: [!DNL Classifications.fin]

Als u uw gegevensbronnen of classificatiebestand uploadt zonder bijbehorend `.fin` -bestand, voegt Adobe dit bestand niet toe aan de wachtrij voor verwerking. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud] . U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt ingevoerd als [!UICONTROL Notification Recipient] in het venster [!UICONTROL Create FTP Account] Analytics. Als in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand uploadt met een `.fin` -bestand, maar er een fout in het bestand staat, wordt het verzonden voor verwerking, maar door de fout wordt de verwerking beëindigd en wordt het bestand verzonden naar een map met foutmeldingen. Als dit gebeurt, wordt een melding verzonden naar het e-mailadres dat wordt vermeld in het veld [!UICONTROL Notification Recipient] in het [!UICONTROL Create FTP Account] -venster. Als er geen e-mailadres is opgegeven, wordt er geen melding verzonden.
