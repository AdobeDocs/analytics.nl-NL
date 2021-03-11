---
description: U kunt Analytics gebruiken om op FTP-Gebaseerde Gegevensbronnen tot stand te brengen en te beheren, die de dossieroverdracht van FTP gebruiken om off-line of historische gegevens in de Experience Cloud in te voeren.
keywords: ftp;sftp
title: Databronnen
uuid: 41ba2de7-d33d-4394-b7d8-04a116f45419
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---


# Databronnen

U kunt Analytics gebruiken om op FTP-Gebaseerde Gegevensbronnen tot stand te brengen en te beheren, die de dossieroverdracht van FTP gebruiken om off-line of historische gegevens in de Experience Cloud in te voeren.

Na het creëren van een instantie van Gegevensbronnen, verstrekt het hulpmiddel een plaats van FTP die u kunt gebruiken om de dossiers van Gegevensbronnen te uploaden. Zodra geupload, vinden de Gegevensbronnen automatisch plaats en verwerken hen. Nadat de bestanden zijn verwerkt, zijn de gegevens beschikbaar voor analytische rapportage.

Het [!UICONTROL Create] lusje in de Manager van Gegevensbronnen laat u een nieuwe instantie van Gegevensbronnen voor de geselecteerde rapportreeks vormen. De [!UICONTROL Data Sources Wizard] begeleidt u door het proces om een malplaatje van Gegevensbronnen tot stand te brengen, en leidt tot een plaats van FTP voor het uploaden van gegevens.

Zoek in het venster [!UICONTROL Manage Data Sources] uw gegevensbron en selecteer de koppeling FTP-info. Uw FTP-aanmeldgegevens worden weergegeven in het venster [!UICONTROL Activate a Data Source] in de sectie [!UICONTROL Upload/FTP Information].

Zie [FTP-limieten en gegevensretentie](/help/export/ftp-and-sftp/ftp-limits.md) voor informatie over FTP-limieten en gegevensretentie.

## Over het .fin-bestand voor classificaties en gegevensbronnen uploadt {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een classificatie of [!UICONTROL Data Source] dossier ( [!DNL .tab] of [!DNL .txt]) uploadt vereist ook dat u een leeg dossier met de nauwkeurige zelfde naam zoals het gegevensdossier uploadt dat, maar met een [!DNL .fin] uitbreiding wordt ingevoerd. Dit [!DNL .fin]-bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. Met het bestand [!DNL .fin] kan Adobe herkennen dat u klaar bent met importeren. Nadat u de bestanden hebt verzonden, verwijdert Adobe beide bestanden van de FTP-server en wordt de importbewerking gestart.
Bestand importeren: [!DNL Classifications.tab]

Bestand voltooien: [!DNL Classifications.fin]

Als u uw Gegevensbronnen of dossier van SAINT zonder begeleidend [!DNL .fin] dossier uploadt, voegt Adobe het niet aan de rij voor verwerking toe. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud]. U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt ingevoerd als [!UICONTROL Notification Recipient] in het venster [!UICONTROL Create FTP Account] voor rapportage. Als er in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand uploadt met een [!DNL .fin]-bestand, maar er een fout in het bestand staat, wordt het ter verwerking verzonden, maar de fout leidt tot het stoppen van de verwerking en het verzenden van het bestand naar een map met foutmeldingen. Als dit voorkomt, wordt een bericht verzonden naar het e-mailadres dat in [!UICONTROL Notification Recipient] gebied in het [!UICONTROL Create FTP Account] venster wordt vermeld. Als er geen e-mailadres wordt opgegeven, wordt er geen melding verzonden.
