---
description: Stappen die beschrijven hoe te om een dossier van gegevensbronnen te uploaden.
title: Een gegevensbronbestand uploaden
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 8b7fa32c-01f2-452b-bf8e-8a81da266926
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 3%

---

# Een gegevensbronbestand uploaden

Nadat u een gegevensdossier van Gegevensbronnen hebt voorbereid, leg het aan Gegevensbronnen voor verwerking voor. Adobe handhaaft verscheidene servers van FTP van Gegevensbronnen waar u de dossiers van Gegevensbronnen kunt uploaden. Herinner het volgende over de servers van FTP van Gegevensbronnen:

* Selecteer FTP-info naast de gegevensbronvermelding in het dialoogvenster [!UICONTROL Data Sources Manage] om de FTP-host, aanmeldingsgegevens en wachtwoordgegevens voor de FTP-account van de gegevensbron weer te geven. Iedereen met toegang tot deze informatie kan gegevens uploaden naar uw rapportsuite.
* Om veiligheidsredenen worden FTP-accounts afgesloten na 30 dagen inactiviteit.
* FTP-accounts zijn specifiek voor de gegevensbron. U kunt geen één rekening van FTP gebruiken om de dossiers van Gegevensbronnen aan veelvoudige gegevensbronnen te uploaden.

**Een gegevensbronbestand uploaden**

1. Gebruik een FTP-client om de gegevens naar uw FTP-site met gegevensbronnen te verzenden.

   (Beschikbaar in de verbinding van FTP Info in de Manager van Gegevensbronnen).

1. Een [!DNL .fin] dossier om Adobe mee te delen dat de het dossierupload van Gegevensbronnen volledig is.

   De [!DNL .fin] bestand moet precies dezelfde naam hebben als het gegevensbronbestand, behalve voor de bestandsextensie. Adobe plaatst niet het Brondossier van Gegevens voor verwerking tot u uploadt [!DNL .fin] bestand.

   Upload het bestand pas nadat alle gegevensbronbestanden zijn geüpload. Anders, zouden de Gegevensbronnen kunnen proberen om een onvolledig dossier te verwerken.
1. Nadat het .fin- dossier wordt geupload, is het belangrijk dat u zich uit de plaats van FTP van Gegevensbronnen afmeldt. De reden is dat Analytics logout-gebeurtenissen gebruikt als trigger om aan te geven dat bestanden klaar zijn voor verwerking.
1. Controle voor om het even welke berichten tijdens de het dossierverwerking van Gegevensbronnen.

   De Manager van Gegevensbronnen toont om het even welke fouten die tijdens de dossierverwerking voorkomen.
