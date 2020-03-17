---
description: De optie SAINT (Classifications) FTP biedt meer flexibiliteit bij het uploaden van grote sets classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en om gegevenssets te uploaden die groter zijn dan 50.000 rijen.
keywords: ftp;sftp
title: Classificaties
uuid: 35936c98-b785-43eb-89f4-ab42a10db256
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Classificaties

De FTP-optie voor classificaties biedt meer flexibiliteit bij het uploaden van grote sets met classificatiegegevens, zoals de mogelijkheid om gegevens te uploaden naar meerdere rapportsets en gegevenssets te uploaden die groter zijn dan 50.000 rijen.

Zie [classificaties](https://marketing.adobe.com/resources/help/en_US/reference/c_working_with_saint.html) voor stappen over het downloaden van classificatiegegevens via FTP en het uploaden van gegevensbestanden via FTP (inclusief de stappen om een FTP-account te maken).

De tijd die het systeem nodig heeft om deze bestanden te importeren, varieert op basis van een aantal factoren. Als er na zes uur nog een geüpload bestand aanwezig is op de FTP-server, kunt u contact opnemen met de door uw organisatie ondersteunde gebruikers voor de klantenservice van Adobe.

Wanneer het importeren is gelukt, worden direct de juiste wijzigingen in een exportbewerking weergegeven, terwijl het wijzigen van de gegevens in Analytics maximaal vier uur kan duren bij het importeren van een browser en maximaal 24 uur bij het importeren van een FTP-bestand.

Zie [FTP-limieten en gegevensbewaring voor informatie over FTP-limieten en gegevensbewaring](/help/export/ftp-and-sftp/ftp-limits.md).

## Over het .fin-bestand voor classificaties en gegevensbronnen uploaden {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een classificatie of een [!UICONTROL Data Source] dossier ( [!DNL .tab]of [!DNL .txt]) uploadt vereist ook dat u een leeg dossier met de nauwkeurige zelfde naam zoals het gegevensdossier uploadt dat, maar met een [!DNL .fin] uitbreiding wordt ingevoerd. Dit [!DNL .fin] bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. Met dit [!DNL .fin] bestand kan Adobe herkennen dat u klaar bent met importeren. Nadat u de bestanden hebt verzonden, verwijdert Adobe beide bestanden van de FTP-server en wordt de importbewerking gestart.
Bestand importeren: [!DNL Classifications.tab]

Bestand voltooien: [!DNL Classifications.fin]

Als u uw gegevensbronnen of classificatiebestand uploadt zonder bijbehorend [!DNL .fin] bestand, voegt Adobe dit bestand niet toe aan de wachtrij voor verwerking. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud]map. U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt opgegeven als de naam [!UICONTROL Notification Recipient] in het [!UICONTROL Create FTP Account] venster Analytics. Als er in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand wel met een [!DNL .fin] bestand uploadt, maar er een fout in het bestand staat, wordt het ter verwerking verzonden, maar door de fout wordt de verwerking beëindigd en wordt het bestand naar een map met foutmeldingen verzonden. Als dit gebeurt, wordt een bericht verzonden naar het e-mailadres dat in het [!UICONTROL Notification Recipient] veld in het [!UICONTROL Create FTP Account] venster wordt vermeld. Als er geen e-mailadres wordt opgegeven, wordt er geen melding verzonden.
