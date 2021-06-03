---
description: SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. De Diensten van de Techniek van Adobe kunnen opstelling een rekening SFTP om uw gegevens veilig te behouden.
keywords: ftp;sftp
title: Secure File Transfer Protocol - overzicht
uuid: 7dd1a867-e828-4c7b-bf11-75a81d4c149c
exl-id: ea0448f9-1685-4a8f-b2f9-49d315c6ab71
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 9%

---

# Secure File Transfer Protocol - overzicht

SFTP is een veilig protocol voor het overbrengen van gegevens dat ervoor zorgt dat niemand uw gegevens maar u kan zien. De Diensten van de Techniek van Adobe kunnen opstelling een rekening SFTP om uw gegevens veilig te behouden.

## Aflevering onder druk {#section_A47831BB1DCA490BB57F0940617AA506}

Dit betekent dat Adobe het bestand &#39;duwen&#39; op uw servers. In wezen leveren we het aan uw eindpunt.

[Gegevens ](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-dw.md) Warehouse en  [Analytics Data ](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-overview.html) Feedback kan gegevens via SFTP duwen.

De volgende Analytics-gereedschappen **kunnen**-pushgegevens niet via SFTP gebruiken:

* Rapporten en analyses
* Ad Hoc Analysis
* Report Builder

## Volledige aflevering {#section_FA29FAEF02FE40B8B32452146A036F48}

Dit betekent dat het bestand naar een van de servers van de Adobe wordt verzonden met normale FTP. Als u het bestand op uw server wilt plaatsen, moet u het bestand via SFTP van de server naar de FTP-server van Adobe halen. U kunt dit op een van de volgende drie manieren doen:

* [Verbinding maken met Adobe via SFTP zonder wachtwoord.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
* [Maak verbinding met een Adobe FTP-account met SFTP.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
* U kunt rapporten duwen u FTP-als gegevensvoer wilt Adobe/R&amp;A/Ad Hoc, etc. en dan hen wegtrekken. Adobe kan deze rapporten niet leveren aan de SFTP-server die u hebt ingesteld.
