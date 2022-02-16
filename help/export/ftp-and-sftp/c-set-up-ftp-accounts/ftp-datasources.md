---
description: U kunt Analytics gebruiken om op FTP-Gebaseerde Gegevensbronnen tot stand te brengen en te beheren, die de dossieroverdracht van FTP gebruiken om off-line of historische gegevens in de Experience Cloud in te voeren.
keywords: ftp;sftp
title: Databronnen
feature: FTP Export
exl-id: 777917bd-bd11-4360-a149-e4fd0bb2f99e
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 0%

---

# Databronnen

U kunt Analytics gebruiken om op FTP-Gebaseerde Gegevensbronnen tot stand te brengen en te beheren, die de dossieroverdracht van FTP gebruiken om off-line of historische gegevens in de Experience Cloud in te voeren.

Na het creëren van een instantie van Gegevensbronnen, verstrekt het hulpmiddel een plaats van FTP die u kunt gebruiken om de dossiers van Gegevensbronnen te uploaden. Zodra geupload, vinden de Gegevensbronnen automatisch plaats en verwerken hen. Nadat de bestanden zijn verwerkt, zijn de gegevens beschikbaar voor analytische rapportage.

De [!UICONTROL Create] het lusje in de Manager van Gegevensbronnen laat u een nieuwe instantie van Gegevensbronnen voor de geselecteerde rapportreeks vormen. De [!UICONTROL Data Sources Wizard] begeleidt u door het proces om een malplaatje van Gegevensbronnen tot stand te brengen, en leidt tot een plaats van FTP voor het uploaden van gegevens.

In de [!UICONTROL Manage Data Sources] , zoekt u de gegevensbron en selecteert u de koppeling FTP-info. Uw FTP-aanmeldgegevens worden weergegeven in het dialoogvenster [!UICONTROL Activate a Data Source] in het [!UICONTROL Upload/FTP Information] sectie.

Voor informatie over FTP-beperkingen en gegevensbehoud raadpleegt u [FTP-limieten en gegevensbewaring](/help/export/ftp-and-sftp/ftp-limits.md).

## Over het .fin-bestand voor classificaties en gegevensbronnen uploaden {#section_1484719F8A134EAE91212DBD8F15174F}

Wanneer u een classificatie uploadt of [!UICONTROL Data Source] file ( [!DNL .tab] of [!DNL .txt]) uploadt u ook een leeg bestand met dezelfde naam als het gegevensbestand dat wordt geïmporteerd, maar met een [!DNL .fin] extensie. Dit [!DNL .fin] bestand is een voltooid bestand. Het doel van het bestand is om het systeem te laten weten dat het gegevensbestand volledig is geüpload naar de FTP-account. De [!DNL .fin] kan Adobe zien dat u klaar bent met importeren. Nadat u de bestanden hebt verzonden, verwijdert Adobe beide bestanden van de FTP-server en wordt de importbewerking gestart.
Bestand importeren: [!DNL Classifications.tab]

Bestand voltooien: [!DNL Classifications.fin]

Als u een gegevensbron- of SAINT-bestand uploadt zonder dat u een [!DNL .fin] -bestand, voegt Adobe deze niet toe aan de wachtrij voor verwerking. Het bestand blijft op de FTP en wordt niet toegepast op de gegevens in de [!UICONTROL Experience Cloud]. U wordt hiervan alleen op de hoogte gesteld als u uw e-mailadres hebt ingevoerd als de [!UICONTROL Notification Recipient] in de [!UICONTROL Create FTP Account] rapportagevenster. Als er in dit veld geen e-mailadres wordt opgegeven, wordt geen melding verzonden.

Als u het bestand uploadt met een [!DNL .fin] -bestand, maar er is een fout in het bestand. Het bestand wordt ter verwerking verzonden, maar door de fout wordt de verwerking beëindigd en het bestand naar een map met foutmeldingen verzonden. Als dit gebeurt, wordt een melding verzonden naar het e-mailadres dat in de [!UICONTROL Notification Recipient] in het [!UICONTROL Create FTP Account] venster. Als er geen e-mailadres wordt opgegeven, wordt er geen melding verzonden.
