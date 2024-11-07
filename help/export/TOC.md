---
product: analytics
audience: end-user
user-guide-title: Handleiding voor exporteren van analysemogelijkheden
breadcrumb-title: Handleiding exporteren
user-guide-description: Leer meer over het gebruik van datafeeds om onbewerkte gegevens te exporteren en Data Warehouse om een spreadsheetuitvoer van gegevens op te halen. Meer informatie over FTP en SFTP gebruiken om bestanden over te dragen.
source-git-commit: aac5421b658cf06b20ca5a3d22f07ef441283753
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 23%

---


# Adobe Analytics Export Guide {#export}

+ [Handleiding voor exporteren van analysemogelijkheden](home.md)
+ [ de Nota&#39;s van de Versie van Analytics ](https://experienceleague.adobe.com/docs/analytics/release-notes/latest.html)
+ Gegevensfeed Analytics {#analytics-data-feed}
   + [Overzicht van gegevensinvoer](analytics-data-feed/data-feed-overview.md)
   + [Een gegevensfeed maken](analytics-data-feed/create-feed.md)
   + [Gegevensfeeds beheren](analytics-data-feed/df-manage-feeds.md)
   + [Taken voor gegevensinvoer beheren](analytics-data-feed/df-manage-jobs.md)
   + Inhoud van gegevensfeed {#data-feed-contents}
      + [Overzicht van de inhoud van de gegevensfeed](analytics-data-feed/c-df-contents/datafeeds-contents.md)
      + [Metrische gegevens berekenen](analytics-data-feed/c-df-contents/datafeeds-calculate.md)
      + [Referentie gegevenskolom](analytics-data-feed/c-df-contents/datafeeds-reference.md)
      + [Opzoeken van paginagebeurtenissen](analytics-data-feed/c-df-contents/datafeeds-page-event.md)
      + [Dynamische zoekopdrachten](analytics-data-feed/c-df-contents/dynamic-lookups.md)
      + [Opzoekopdracht eVar wijzigen](analytics-data-feed/c-df-contents/merchandising-evar-lookup.md)
      + [Speciale tekens](analytics-data-feed/c-df-contents/datafeeds-spec-chars.md)
      + [Te laat arriveren](analytics-data-feed/c-df-contents/late-arriving-hits.md)
   + [Veelgestelde vragen over gegevensinvoer](analytics-data-feed/df-faq.md)
   + [Aanbevolen werkwijzen voor gegevensinvoer](analytics-data-feed/data-feeds-best-practices.md)
   + [Gegevensfeeds oplossen](analytics-data-feed/troubleshooting.md)
+ Data Warehouse {#data-warehouse}
   + [Overzicht van Data Warehouse](data-warehouse/data-warehouse.md)
   + [Gebruikersgroep Data Warehouse toevoegen](data-warehouse/t-dw-group.md)
   + Een Data Warehouse-aanvraag maken {#dw-create-request}
      + [Een Data Warehouse-aanvraag maken](/help/export/data-warehouse/create-request/t-dw-create-request.md)
      + [Algemene instellingen](/help/export/data-warehouse/create-request/dw-general-settings.md)
      + [Uw rapport samenstellen](/help/export/data-warehouse/create-request/dw-request-build-report.md)
      + [Doel van rapport](/help/export/data-warehouse/create-request/dw-request-report-destinations.md)
      + [Rapportopties](/help/export/data-warehouse/create-request/dw-request-report-options.md)
      + [Planningsopties](/help/export/data-warehouse/create-request/dw-request-scheduling.md)
      + [Bericht](/help/export/data-warehouse/create-request/dw-request-email.md)
   + [Leveringstijd aanvraag](data-warehouse/delivery-time.md)
   + [Tableau-gegevensbestand](data-warehouse/t-tableau.md)
   + [Sorteren op metrisch](data-warehouse/sorting-by-metric.md)
   + [Aanvragen voor Data Warehouse beheren](data-warehouse/data-warehouse-requests-manage.md)
   + [Componenten die worden ondersteund in Data Warehouse](data-warehouse/component-support.md)
   + [Aanbevolen werkwijzen voor Data Warehouse](data-warehouse/data-warehouse-bp.md)
+ FTP en SFTP {#ftp-and-sftp}
   + [FTP en SFTP gebruiken met de Adobe Experience Cloud](ftp-and-sftp/ftp-overview.md)
   + Door Adobe gehoste FTP-accounts instellen {#set-up-ftp-accounts}
      + [FTP-accounts instellen - overzicht](ftp-and-sftp/c-set-up-ftp-accounts/ftp-accounts.md)
      + [Classificaties](ftp-and-sftp/c-set-up-ftp-accounts/ftp-saint.md)
      + [Databronnen](ftp-and-sftp/c-set-up-ftp-accounts/ftp-datasources.md)
      + [Gegevensfeeds](ftp-and-sftp/c-set-up-ftp-accounts/ftp-datafeeds.md)
      + [Door Data Warehouse geleverde rapporten](ftp-and-sftp/c-set-up-ftp-accounts/ftp-dw-reports.md)
      + [Door de Report Builder ingediende rapporten](ftp-and-sftp/c-set-up-ftp-accounts/ftp-arb-reports.md)
      + [Engineering Services-services met FTP](ftp-and-sftp/c-set-up-ftp-accounts/ftp-eng-services.md)
   + [FTP-beperkingen en gegevensopslag](ftp-and-sftp/ftp-limits.md)
   + [FTP-gegevens en FTP-accounts verwijderen](ftp-and-sftp/ftp-delete.md)
   + [Verwijderde FTP-gegevens en FTP-accounts herstellen](ftp-and-sftp/ftp-restore.md)
   + [FTP-servers voor Adobe upgraden](ftp-and-sftp/ftp-upgrade.md)
   + [De passieve FTP-modus gebruiken](ftp-and-sftp/ftp-passive.md)
   + [FTP-verwerkingstijd](ftp-and-sftp/ftp-processing.md)
   + Secure File Transfer Protocol {#secure-file-transfer-protocol}
      + [Upgrade van SFTP-services - Veelgestelde vragen](ftp-and-sftp/c-sftp/sftp-upgrade.md)
      + [Secure File Transfer Protocol - overzicht](ftp-and-sftp/c-sftp/ftp-sftp.md)
      + [Verbinding maken met een Adobe FTP-account met SFTP](ftp-and-sftp/c-sftp/ftp-sftp-connect.md)
      + [Gegevens van Adobe verzenden naar een externe FTP-account met SFTP](ftp-and-sftp/c-sftp/ftp-sftp-transfer.md)
      + [Data Warehouse-aanvragen naar SFTP-servers verzenden](ftp-and-sftp/c-sftp/ftp-sftp-dw.md)
      + [Verbinding maken met Adobe via SFTP zonder wachtwoord](ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md)
+ [ downloads van Analysis Workspace ](https://experienceleague.adobe.com/docs/analytics/analyze/analysis-workspace/curate-share/download-send.html)
+ [ Adobe Analytics API ](https://www.adobe.io/apis/experiencecloud/analytics/docs.html)
+ [ Report Builder ](https://experienceleague.adobe.com/en/docs/analytics/analyze/report-builder/report-buider-overview)
