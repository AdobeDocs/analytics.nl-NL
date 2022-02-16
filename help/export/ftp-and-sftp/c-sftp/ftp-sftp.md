---
description: SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. De Diensten van de Techniek van Adobe kunnen opstelling een rekening SFTP om uw gegevens veilig te behouden.
keywords: ftp;sftp
title: Secure File Transfer Protocol - overzicht
feature: FTP Export
exl-id: ea0448f9-1685-4a8f-b2f9-49d315c6ab71
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 9%

---

# Secure File Transfer Protocol - overzicht

SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. De Diensten van de Techniek van Adobe kunnen opstelling een rekening SFTP om uw gegevens veilig te behouden.

## Aflevering onder druk {#section_A47831BB1DCA490BB57F0940617AA506}

Dit betekent dat Adobe het bestand &#39;duwen&#39; op uw servers. In wezen leveren we het aan uw eindpunt.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) en [Gegevensfeed Analytics](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html) gegevens via SFTP kunnen verzenden.

De volgende analysefuncties **kan** pushgegevens via SFTP:

* Rapporten en analyses
* Ad Hoc Analysis
* Report Builder

## Volledige aflevering {#section_FA29FAEF02FE40B8B32452146A036F48}

Dit betekent dat het bestand naar een van de servers van de Adobe wordt verzonden met normale FTP. Als u het bestand op uw server wilt plaatsen, moet u het bestand via SFTP van de server naar de FTP-server van Adobe halen. U kunt dit op een van de volgende drie manieren doen:

* [Verbinding maken met Adobe via SFTP zonder wachtwoord.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Maak verbinding met een Adobe FTP-account met SFTP.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* U kunt rapporten duwen u FTP-als gegevensvoer wilt Adobe/R&amp;A/Ad Hoc, etc. en dan hen wegtrekken. Adobe kan deze rapporten niet leveren aan de SFTP-server die u hebt ingesteld.
