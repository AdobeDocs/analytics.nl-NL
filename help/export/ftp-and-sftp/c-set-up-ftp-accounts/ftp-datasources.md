---
description: Met Analytics kunt u op FTP gebaseerde gegevensbronnen maken en beheren. Hierbij wordt de bestandsoverdracht via FTP gebruikt om offline of historische gegevens te importeren in de Experience Cloud.
keywords: ftp;sftp
title: Gegevensbronnen
uuid: 41ba2de7-d33d-4394-b7d8-04a116f45419
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Gegevensbronnen

Met Analytics kunt u op FTP gebaseerde gegevensbronnen maken en beheren. Hierbij wordt de bestandsoverdracht via FTP gebruikt om offline of historische gegevens te importeren in de Experience Cloud.

Na het creëren van een instantie van Gegevensbronnen, verstrekt het hulpmiddel een plaats van FTP die u kunt gebruiken om de dossiers van Gegevensbronnen te uploaden. Zodra geupload, vinden de Gegevensbronnen automatisch plaats en verwerken hen. Nadat de bestanden zijn verwerkt, zijn de gegevens beschikbaar voor analytische rapportage.

Het [!UICONTROL Create] lusje in de Manager van Gegevensbronnen laat u een nieuwe instantie van Gegevensbronnen voor de geselecteerde rapportreeks vormen. De [!UICONTROL Data Sources Wizard] begeleidt u door het proces om een malplaatje van Gegevensbronnen te creëren, en leidt tot een plaats van FTP voor het uploaden van gegevens.

Zoek in het [!UICONTROL Manage Data Sources] venster uw gegevensbron en selecteer de koppeling FTP-info. De FTP-aanmeldgegevens worden weergegeven in het [!UICONTROL Activate a Data Source] venster in de [!UICONTROL Upload/FTP Information] sectie.

Zie [FTP-limieten en gegevensbewaring voor informatie over FTP-limieten en gegevensbewaring](/help/export/ftp-and-sftp/ftp-limits.md).

## Over het .fin-bestand voor classificaties en gegevensbronnen uploaden {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een classificaties of [!UICONTROL Data Source] bestand ( [!DNL .tab] of [!DNL .txt]) uploadt, moet u ook een leeg bestand uploaden met dezelfde naam als het gegevensbestand dat wordt geïmporteerd, maar met een [!DNL .fin] extensie. Dit [!DNL .fin] bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. Met dit [!DNL .fin] bestand kan Adobe herkennen dat u klaar bent met importeren. Nadat u de bestanden hebt verzonden, verwijdert Adobe beide bestanden van de FTP-server en verwerkt het importeren.
Bestand importeren: [!DNL Classifications.tab]

Bestand voltooien: [!DNL Classifications.fin]

Als u uw gegevensbronnen of SAINT-bestand uploadt zonder bijbehorend [!DNL .fin] bestand, voegt Adobe dit bestand niet toe aan de wachtrij voor verwerking. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud]map. U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt opgegeven als de naam [!UICONTROL Notification Recipient] in het [!UICONTROL Create FTP Account] rapportagevenster. Als er in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand wel met een [!DNL .fin] bestand uploadt, maar er een fout in het bestand staat, wordt het ter verwerking verzonden, maar door de fout wordt de verwerking beëindigd en wordt het bestand naar een map met foutmeldingen verzonden. Als dit gebeurt, wordt een bericht verzonden naar het e-mailadres dat in het [!UICONTROL Notification Recipient] veld in het [!UICONTROL Create FTP Account] venster wordt vermeld. Als er geen e-mailadres wordt opgegeven, wordt er geen melding verzonden.
