---
description: Gegevensfeeds zijn een export van de gegevens van de clickstream die door Adobe worden ontvangen en die zowel standaard als aangepaste gegevensfeeds biedt.
keywords: ftp;sftp
title: Gegevensfeeds
feature: FTP Export
exl-id: 286050fa-e197-4b70-b167-da6921615c1b
source-git-commit: 05b4dc07de567b25e71b47fd92743bee0b5621f8
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---

# Gegevensfeeds

>[!NOTE]
>
>De volgende informatie heeft betrekking op FTP- en SFTP-doeltypen. FTP en SFTP zijn oudere doeltypen. Wanneer het vormen van een gegevensvoer, zou u een type van de wolkenbestemming moeten gebruiken, dat veiliger is. Voor meer informatie over het vormen van de types van wolkenbestemming voor een Diervoer van Gegevens, zie [Een gegevensfeed maken](/help/export/analytics-data-feed/create-feed.md).

Gegevensfeeds zijn een export van de gegevens van de clickstream die door Adobe worden ontvangen en die zowel standaard als aangepaste [Gegevensfeeds](/help/export/analytics-data-feed/data-feed-overview.md).

Als u Adobe Data Warehouse hebt aangeschaft, [!UICONTROL Standard Data Feeds] u kunt uw eigen gegevensfeeds voor Analytics instellen. Ze kunnen naar elke FTP-account worden verzonden (een FTP-account dat is ingesteld door Adobe of een externe FTP). Adobe Engineering Services biedt aangepaste [!UICONTROL Data Feeds] dat kan vrijwel elke vorm van verzending zijn .

[!UICONTROL Data Feed] FTP-accounts staan standaard 10 GB toe. Alle andere standaard FTP-accounts zijn standaard 50 MB. In gevallen waarin clients de FTP-account gebruiken voor het juiste gebruik waarvoor deze bestemd is, kunnen sommige gebruikers met hoge verkeersvolumes deze accounts snel invullen. Wanneer een FTP-account vol is, kunnen er geen extra bestanden naar deze account worden geduwd. Alle bestanden die worden geleverd aan die FTP-account ( [!UICONTROL Data Feeds], de verzoeken van het gegevenspakhuis, enzovoort) niet worden geleverd. Daarom is het belangrijk om uw Adobe FTP-account te beheren door ontvangen en gedownloade bestanden te verwijderen.

Wanneer een FTP-account vol is, moet u de huidige bestanden downloaden en verwijderen en de Adobe laten weten dat de ruimte is gewist. Adobe kan vervolgens bestanden die niet zijn geleverd opnieuw verzenden. Sommige hulpmiddelen, zoals gegevenspakhuis, laten gebruikers deze dossiers opnieuw verzenden. Voor het opnieuw verzenden is mogelijk geen betrokkenheid van de Adobe nodig. Als uw FTP-account vaak wordt ingevuld, neemt u contact op met de klantenservice van Adobe. Hier kunt u leveringsalternatieven voorstellen, zoals een verhoging van de FTP-ruimte en het quotum voor het bestandsnummer van de account.
