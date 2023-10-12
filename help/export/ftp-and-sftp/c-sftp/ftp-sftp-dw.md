---
description: Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.
keywords: ftp;sftp
title: Verstuur de verzoeken van het Data Warehouse naar servers SFTP
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
source-git-commit: d8bfad5d388f906c7c7301a9126813f5c2a5dbaa
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 5%

---

# Verstuur de verzoeken van het Data Warehouse naar servers SFTP

Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers, zoals beschreven in [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp) in het artikel [Vorm een rapportbestemming voor een verzoek van de Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md).

Controleer of de volgende taken zijn voltooid:

* Slechts wordt haven 22 gebruikt wanneer het verzoeken van een rapport van de Data Warehouse.
* Adobe `authorized_keys` bestand bevindt zich in het `.ssh` in de hoofdmap van de gebruiker waarmee u zich aanmeldt.
* De bestemming is niet aan `ftp.omniture.com`. SFTP-protocol tussen interne servers van Adobe wordt niet ondersteund.
* De bestemming steunt één-factor (PKI) authentificatie. Als er een tweeledige uitdaging is, zal de indiening van het verslag mislukken. Zorg ervoor dat uw server niet wordt gevormd om dubbel-factor authentificatie te proberen. Adobe Analytics vereist dat alleen de sleutel en niets anders wordt gebruikt voor aanmelding.
* De Adobe steunt encryptie SSHv2, en valt terug naar SSHv1 (de sleutel van RSA slechts).

Met succes een verzoek van de Data Warehouse via SFTP verzenden:

1. Voer de in [SFTP](/help/export/data-warehouse/create-request/dw-request-report-destinations.md#sftp) in het artikel [Vorm een rapportbestemming voor een verzoek van de Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md), inclusief het downloaden van de openbare sleutel.
1. Meld u aan bij de SFTP-site onder dezelfde referenties die voor het verzoek van de Data Warehouse worden gebruikt.
1. Navigeer in de hoofdmap naar de genoemde map `.ssh` (als er geen bestaat, maakt u er een) en plaatst u de knop `authorized_keys` bestand daar.

1. Vul het verzoek om Data Warehouse in als u dit nog niet hebt gedaan, zoals beschreven in [Vorm een rapportbestemming voor een verzoek van de Data Warehouse](/help/export/data-warehouse/create-request/dw-request-report-destinations.md).
