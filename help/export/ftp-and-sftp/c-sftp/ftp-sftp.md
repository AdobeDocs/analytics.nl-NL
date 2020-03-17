---
description: SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. Adobe Engineering Services kan een SFTP-account instellen om uw gegevens veilig te behouden.
keywords: ftp;sftp
title: Secure File Transfer Protocol - overzicht
uuid: 7dd1a867-e828-4c7b-bf11-75a81d4c149c
translation-type: tm+mt
source-git-commit: ''

---


# Secure File Transfer Protocol - overzicht

SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. Adobe Engineering Services kan een SFTP-account instellen om uw gegevens veilig te behouden.

## Aflevering onder druk {#section_A47831BB1DCA490BB57F0940617AA506}

Dit betekent dat de servers van Adobe het bestand naar uw servers &quot;duwen&quot;. In wezen leveren we het aan uw eindpunt.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) en [Analytics Data Feed](https://marketing.adobe.com/resources/help/en_US/reference/analytics-data-feed.html) kan gegevens via SFTP duwen.

De volgende analysehulpmiddelen **kunnen geen** gegevens via SFTP duwen:

* Rapporten en analyses
* Ad hoc-analyse
* Report Builder

## Volledige aflevering {#section_FA29FAEF02FE40B8B32452146A036F48}

Dit betekent dat het bestand naar een van de servers van Adobe wordt verzonden met normale FTP. Als u het bestand op uw server wilt plaatsen, moet u het van de server van Adobe halen gebruikend SFTP van uw server aan de server van FTP van Adobe. U kunt dit op een van de volgende drie manieren doen:

* [Maak verbinding met Adobe via SFTP zonder wachtwoord.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Maak verbinding met een Adobe FTP-account met SFTP.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* U kunt rapporten duwen u aan FTP-als gegevensvoer/R&amp;A/Ad Hoc van Adobe wilt, etc., en dan hen wegtrekken. Adobe kan deze rapporten niet leveren aan de SFTP-server die u hebt ingesteld.

