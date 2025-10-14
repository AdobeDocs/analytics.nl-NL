---
description: SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. Adobe Engineering Services kan een SFTP-account instellen om uw gegevens veilig te behouden.
keywords: ftp;sftp
title: Secure File Transfer Protocol - overzicht
feature: FTP Export
exl-id: ea0448f9-1685-4a8f-b2f9-49d315c6ab71
source-git-commit: fcc165536d77284e002cb2ba6b7856be1fdb3e14
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# Secure File Transfer Protocol - overzicht

SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. Adobe Engineering Services kan een SFTP-account instellen om uw gegevens veilig te behouden.

## Aflevering onder druk {#section_A47831BB1DCA490BB57F0940617AA506}

Dit betekent dat Adobe-servers het bestand naar uw servers &#39;duwen&#39;. In wezen leveren we het aan uw eindpunt.

[&#x200B; Data Warehouse &#x200B;](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) en [&#x200B; Diervoed van Gegevens van de Analyse &#x200B;](/help/export/analytics-data-feed/data-feed-overview.md) kan gegevens via SFTP duwen.

Report Builder **kan** duw geen gegevens via SFTP.

## Volledige aflevering {#section_FA29FAEF02FE40B8B32452146A036F48}

Dit betekent dat het bestand naar een van de Adobe-servers wordt verzonden met normale FTP. Als u het bestand op uw server wilt plaatsen, moet u het van de Adobe-server halen met behulp van SFTP van uw server naar de Adobe FTP-server. U kunt dit op een van de volgende drie manieren doen:

* [&#x200B; verbind met Adobe via SFTP zonder een wachtwoord.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [&#x200B; verbind met een Rekening van FTP van Adobe met SFTP.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* U kunt op rapporten drukken die u op FTP-achtige gegevensfeeds/R&amp;A/Ad Hoc wilt Adobe, enzovoort, en deze vervolgens wegtrekken. Adobe kan deze rapporten niet leveren aan de SFTP-server die u hebt ingesteld.
