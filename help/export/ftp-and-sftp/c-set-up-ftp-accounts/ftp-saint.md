---
description: De optie FTP voor classificaties (SAINT) biedt meer flexibiliteit bij het uploaden van grote sets met classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en om gegevenssets te uploaden die groter zijn dan 50.000 rijen.
keywords: ftp;sftp
title: Classificaties
uuid: 35936c98-b785-43eb-89f4-ab42a10db256
translation-type: tm+mt
source-git-commit: 7a70a5185b768dbc09deca5c8989693501af0cca
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 2%

---


# Classificaties

De FTP-optie voor classificaties biedt meer flexibiliteit bij het uploaden van grote sets met classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en gegevenssets te uploaden die groter zijn dan 50.000 rijen.

Zie [classificaties](https://docs.adobe.com/content/help/en/analytics/components/classifications/classifications-importer/c-working-with-saint.html) voor stappen over het downloaden van classificatiegegevens via FTP en het uploaden van gegevensbestanden via FTP (inclusief de stappen om een FTP-account te maken).

De tijd die het systeem nodig heeft om deze bestanden te importeren, varieert op basis van een aantal factoren. Als een geüpload bestand meer dan drie dagen op de FTP-server aanwezig is, kunt u contact opnemen met de door uw organisatie ondersteunde gebruikers om contact op te nemen met de klantenservice van Adobe.

Wanneer het importeren is gelukt, worden direct de juiste wijzigingen in een exportbewerking weergegeven, terwijl het wijzigen van de gegevens in Analytics maximaal vier uur kan duren bij het importeren van een browser en maximaal 24 uur bij het importeren van een FTP-bestand.

Zie [FTP-limieten en gegevensbewaring voor informatie over FTP-limieten en gegevensbewaring](/help/export/ftp-and-sftp/ftp-limits.md).

## Over het `.fin` bestand voor classificaties en gegevensbronnen uploaden {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een classificatie- of gegevensbronbestand (`.tab` of `.txt`) uploadt, moet u voor het uploaden ook een leeg bestand uploaden met dezelfde naam als het gegevensbestand dat wordt geïmporteerd, maar met een .`.fin` extensie. Dit `.fin` bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. In het `.fin` bestand kan Adobe zien dat u klaar bent met importeren.

Nadat u zowel het bronbestand als het `.fin` bestand hebt verzonden, is het belangrijk dat u zich afmeldt bij de FTP-site. De reden hiervoor is dat Adobe Analytics logout-gebeurtenissen gebruikt als een trigger waarmee bestanden kunnen worden verwerkt. Nadat het importeren is voltooid, verwijdert Adobe beide bestanden van de FTP-locatie.

Bestand voltooien: [!DNL Classifications.fin]

Als u uw Gegevensbronnen of het dossier van de Classificatie zonder een begeleidend `.fin` dossier uploadt, voegt Adobe het niet aan de rij voor verwerking toe. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud]map. U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt opgegeven als de naam [!UICONTROL Notification Recipient] in het [!UICONTROL Create FTP Account] venster Analytics. Als er in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand wel met een `.fin` bestand uploadt, maar er een fout in het bestand staat, wordt het ter verwerking verzonden, maar door de fout wordt de verwerking beëindigd en wordt het bestand naar een map met foutmeldingen verzonden. Als dit gebeurt, wordt een bericht verzonden naar het e-mailadres dat in het [!UICONTROL Notification Recipient] veld in het [!UICONTROL Create FTP Account] venster wordt vermeld. Als er geen e-mailadres is opgegeven, wordt er geen melding verzonden.
