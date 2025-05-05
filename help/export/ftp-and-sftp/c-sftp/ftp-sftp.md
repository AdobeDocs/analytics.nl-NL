---
description: SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. De Diensten van de Techniek van de Adobe kunnen opstelling een rekening SFTP om uw gegevens veilig te behouden.
keywords: ftp;sftp
title: Secure File Transfer Protocol - overzicht
feature: FTP Export
exl-id: ea0448f9-1685-4a8f-b2f9-49d315c6ab71
source-git-commit: 93099d36a65ca2bf16fbd6342f01bfecdc8c798e
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Secure File Transfer Protocol - overzicht

SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. De Diensten van de Techniek van de Adobe kunnen opstelling een rekening SFTP om uw gegevens veilig te behouden.

## Aflevering onder druk {#section_A47831BB1DCA490BB57F0940617AA506}

Dit betekent dat de servers van de Adobe het bestand naar uw servers &quot;duwen&quot;. In wezen leveren we het aan uw eindpunt.

[Data Warehouse](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) en [Gegevensfeed Analytics](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html?lang=nl-NL) gegevens via SFTP kunnen verzenden.

Report Builder **kan** pushgegevens via SFTP.

## Volledige aflevering {#section_FA29FAEF02FE40B8B32452146A036F48}

Dit betekent dat het bestand naar een van de servers van de Adobe wordt verzonden met normale FTP. Als u het bestand op uw server wilt plaatsen, moet u het van de server van de Adobe halen gebruikend SFTP van uw server aan de server van FTP van de Adobe. U kunt dit op een van de volgende drie manieren doen:

* [Verbinding maken met Adobe via SFTP zonder wachtwoord.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Verbind met een Rekening van FTP van de Adobe met SFTP.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* U kunt op rapporten drukken die u op FTP-achtige gegevensfeeds/R&amp;A/Ad Hoc van de Adobe wilt weergeven, enzovoort, en deze vervolgens wegtrekken. Adobe kan deze rapporten niet leveren aan de SFTP-server die u hebt ingesteld.
