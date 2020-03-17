---
description: Stappen die beschrijven hoe te om een dossier van gegevensbronnen te uploaden.
subtopic: Data sources
title: Een gegevensbronbestand uploaden
topic: Developer and implementation
uuid: 5a9dde91-1297-47e5-9393-611b40413c17
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Een gegevensbronbestand uploaden

Stappen die beschrijven hoe te om een dossier van gegevensbronnen te uploaden.

Nadat u een gegevensdossier van Gegevensbronnen hebt voorbereid, leg het aan Gegevensbronnen voor verwerking voor. Adobe onderhoudt verschillende FTP-servers voor gegevensbronnen waar u gegevensbronbestanden kunt uploaden. Herinner het volgende over de servers van FTP van Gegevensbronnen:

* Selecteer FTP-info naast de gegevensbronvermelding op het [!UICONTROL Data Sources Manage] tabblad om de FTP-host, aanmelding en wachtwoordinformatie voor de FTP-account van de gegevensbron weer te geven. Iedereen met toegang tot deze informatie kan gegevens uploaden naar uw rapportsuite.
* Om veiligheidsredenen worden FTP-accounts afgesloten na 30 dagen inactiviteit.
* FTP-accounts zijn specifiek voor de gegevensbron. U kunt geen één rekening van FTP gebruiken om de dossiers van Gegevensbronnen aan veelvoudige gegevensbronnen te uploaden.

**Een gegevensbronbestand uploaden**

1. Gebruik een FTP-client om de gegevens naar uw FTP-site met gegevensbronnen te verzenden.

   (Beschikbaar in de verbinding van FTP Info in de Manager van Gegevensbronnen).

1. Upload een [!DNL .fin] bestand om Adobe te laten weten dat het uploaden van het gegevensbronbestand is voltooid.

   Het [!DNL .fin] bestand moet precies dezelfde naam hebben als het gegevensbronbestand, behalve voor de bestandsextensie. Adobe plaatst het gegevensbronbestand niet in de wachtrij voor verwerking totdat u het [!DNL .fin] bestand uploadt.

   Upload het bestand pas nadat alle gegevensbronbestanden zijn geüpload. Anders, zouden de Gegevensbronnen kunnen proberen om een onvolledig dossier te verwerken.
1. Controle voor om het even welke berichten tijdens de het dossierverwerking van Gegevensbronnen.

   De Manager van Gegevensbronnen toont om het even welke fouten die tijdens de dossierverwerking voorkomen.

