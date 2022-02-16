---
description: De optie FTP voor classificaties (SAINT) biedt meer flexibiliteit bij het uploaden van grote sets met classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en om gegevenssets te uploaden die groter zijn dan 50.000 rijen.
keywords: ftp;sftp
title: Classificaties
feature: FTP Export
exl-id: fc783328-a70b-4af3-b3d3-c59ab79d6b8f
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 0%

---

# Classificaties

De FTP-optie voor classificaties biedt meer flexibiliteit bij het uploaden van grote sets met classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en gegevenssets te uploaden die groter zijn dan 50.000 rijen.

Zie [classificaties](https://experienceleague.adobe.com/docs/analytics/components/classifications/classifications-importer/c-working-with-saint.html) voor stappen voor het downloaden van classificatiegegevens via FTP en het uploaden van gegevensbestanden via FTP (inclusief de stappen voor het maken van een FTP-account).

De tijd die het systeem nodig heeft om deze bestanden te importeren, varieert op basis van een aantal factoren. Als een geüpload bestand meer dan drie dagen op de FTP-server aanwezig is, kunt u contact opnemen met de door uw organisatie ondersteunde gebruikers om contact op te nemen met de klantenservice van Adobe.

Wanneer het importeren is gelukt, worden direct de juiste wijzigingen in een exportbewerking weergegeven, terwijl het wijzigen van de gegevens in Analytics maximaal vier uur kan duren bij het importeren van een browser en maximaal 24 uur bij het importeren van een FTP-bestand.

Voor informatie over FTP-beperkingen en gegevensbehoud raadpleegt u [FTP-limieten en gegevensbewaring](/help/export/ftp-and-sftp/ftp-limits.md).

## Over het `.fin` bestand voor classificaties en gegevensbronnen uploaden {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een classificatie- of gegevensbronbestand uploadt (`.tab` of `.txt`), moet u voor het uploaden ook een leeg bestand uploaden met dezelfde naam als het gegevensbestand dat wordt geïmporteerd, maar met een naam.`.fin` extensie. Dit `.fin` bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. De `.fin` kan Adobe zien dat u klaar bent met importeren.

Nadat u zowel het bronbestand als het `.fin` is het belangrijk om u af te melden bij de FTP-site. De reden hiervoor is dat Adobe Analytics logout-gebeurtenissen gebruikt als een trigger waarmee bestanden kunnen worden verwerkt. Nadat het importeren is voltooid, verwijdert Adobe beide bestanden van de FTP-locatie.

Bestand voltooien: [!DNL Classifications.fin]

Als u uw gegevensbronnen of classificatiebestand uploadt zonder dat u een `.fin` -bestand, voegt Adobe deze niet toe aan de wachtrij voor verwerking. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud]. U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt ingevoerd als de [!UICONTROL Notification Recipient] in de [!UICONTROL Create FTP Account] venster van Analytics. Als er in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand uploadt met een `.fin` -bestand, maar er is een fout in het bestand. Het bestand wordt ter verwerking verzonden, maar door de fout wordt de verwerking beëindigd en het bestand naar een map met foutmeldingen verzonden. Als dit gebeurt, wordt een melding verzonden naar het e-mailadres dat in de [!UICONTROL Notification Recipient] in het [!UICONTROL Create FTP Account] venster. Als er geen e-mailadres is opgegeven, wordt er geen melding verzonden.
