---
title: Gegevensbronnen beheren
description: Navigeren de interface voor het beheren van gegevensbronnen.
exl-id: 315501fb-26e1-436a-938d-5957ca037cd0
feature: Data Sources
role: Admin
source-git-commit: 27bcbd638848650c842ad8d8aaa7ab59e27e900e
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# Gegevensbronnen beheren

Met de gegevensbronmanager kunt u gegevensbronnen maken, bewerken of deactiveren. U kunt deze interface ook gebruiken om de status bij te houden van bestanden die naar FTP-locaties met gegevensbronnen zijn geüpload.

**[!UICONTROL Admin]** > **[!UICONTROL All Admin]** > **[!UICONTROL Data sources]**

Gebruik de selecteur van de rapportreeks in het hoogste recht om tussen rapportreeksen in uw organisatie te schakelen.

Er zijn drie belangrijkste lusjes aan deze interface; **[!UICONTROL Manage]**, **[!UICONTROL Create]**, en **[!UICONTROL File Log]**.

## Beheren

De **[!UICONTROL Manage]** worden alle gegevensbronnen verwerkt die uw organisatie heeft gemaakt. U kunt FTP-informatie weergeven, bewerkingen uitvoeren op variabelen die in sjabloonbestanden worden gebruikt of gegevensbronnen volledig deactiveren.

![Beheren](assets/manage.png)

De bovenste gegevensbron is altijd [!UICONTROL Web Beacon]. Deze gegevensbron is wat u voor typische gegevensinzameling door AppMeasurement gebruikt. Kan niet bewerken of deactiveren.

Elke gegevensbron heeft de volgende opties:

* **[!UICONTROL Restart Processing]**: Start gegevensbronverwerking die eerder is gestopt als gevolg van fouten. De verwerking gaat door tot de volgende fout wordt ontmoet. Gegevensbronnen stoppen de verwerking van een gegevensbronbestand alleen wanneer u **[!UICONTROL Stop processing on errors]**.
* **[!UICONTROL Complete Processing]**: Niet meer gebruikt - deze knop wordt alleen gebruikt voor [Volledige verwerkingsgegevensbronnen](full-processing-eol.md).
* **[!UICONTROL Stop processing on errors]**: Een selectievakje waarmee de verwerkingsserver wordt opgedragen te stoppen wanneer een fout optreedt. De gegevensbron hervat geen verwerking tot u selecteert **[!UICONTROL Restart Processing]**. Wanneer een gegevensbron een dossierfout ontmoet, brengt het u op de hoogte van de fout. Adobe verplaatst het bestand met de fout naar een map met de naam `files_with_errors` op de FTP-server. Nadat u het probleem hebt opgelost, dient u het bestand opnieuw in voor verwerking.
* **[!UICONTROL Configure]**: Een koppeling die u door de wizard Gegevensbronnen maakt voor deze gegevensbron. Met deze wizard kunt u de naam van de gegevensbron wijzigen of de variabelen die automatisch worden opgenomen tijdens het downloaden van een sjabloonbestand opnieuw configureren.
* **[!UICONTROL FTP Info]**: Een koppeling die u naar de laatste stap van de wizard Gegevensbronnen maakt waar FTP-referenties worden weergegeven.

Zodra een gegevensbron gegevens ontvangt, wordt een lijst getoond die verscheidene kolommen voor de geupload dossiers bevat.

* **[!UICONTROL Files In Processing Queue]**: De naam van het bestand.
* **[!UICONTROL Rows]**: Het totale aantal rijen in het bestand.
* **[!UICONTROL Errors]**: Het aantal rijen dat fouten bevatte en niet kon worden opgenomen.
* **[!UICONTROL Warnings]**: Het aantal rijen met waarschuwingen.
* **[!UICONTROL Received]**: De tijdstempel dat het bestand is ontvangen in de tijdzone van de rapportsuite.
* **[!UICONTROL Status]**: De status van het bestand (`Success` of `Failed`).

## Maken

De **[!UICONTROL Create]** biedt u een beginpunt voor de wizard Gegevensbronnen maken.

![Maken](assets/create.png)

De categorie en het type van gegevensbron waren waardevoller in vorige versies van Adobe Analytics. Zij hebben echter nog steeds een beperkt gebruik:

* Het gegevenstype van de gegevensbron wordt getoond op [Beheren](#manage) -tabblad voor de gegevensbron zelf, en [Bestandslogbestand](#file-log) voor elk afzonderlijk bestand.
* Sommige gegevensbrontypen bevatten automatisch variabelen wanneer het sjabloonbestand wordt gedownload. Nochtans, kunt u om het even welke beschikbare afmeting of metrisch omvatten zolang het zich aan vastgestelde houdt [Bestandsindeling](file-format.md).

Buiten deze redenen, zijn alle gegevensbroncategorieën en types die u kunt kiezen effectief identiek. Kies de categorie en het type die het beste uw doel voor het gebruik van gegevensbronnen vertegenwoordigen.

Met het terugtrekken van [Volledige verwerkingsgegevensbronnen](full-processing-eol.md), kunnen verschillende categorieën en typen niet worden geselecteerd. Als u een volledig type van verwerkingsgegevensbron selecteert, **[!UICONTROL Activate]** wordt grijs weergegeven.

## Bestandslogbestand

De **[!UICONTROL File Log]** geeft u een samengevoegde mening van alle gegevensbrondossiers die voor de bepaalde rapportreeks worden geupload.

![Bestandslogbestand](assets/file-log.png)

Er is een zoekbalk beschikbaar waarmee u een specifieke gegevensbron kunt zoeken. In de tabel staan de volgende kolommen:

* **[!UICONTROL Data Source Name]**: De naam van de gegevensbron.
* **[!UICONTROL Type]**: Het type gegevensbron.
* **[!UICONTROL Filename]**: De naam van het geüploade bestand.
* **[!UICONTROL Rows]**: Het totale aantal rijen in het bestand.
* **[!UICONTROL Errors]**: Het aantal rijen met fouten.
* **[!UICONTROL Warnings]**: Niet meer gebruikt. Het aantal rijen dat waarschuwingen bevatte.
* **[!UICONTROL Received]**: De datum en tijd waarop de Adobe is begonnen met het verwerken van het bestand.
* **[!UICONTROL Status]**: De status van het bestand (`Success` of `Failed`).
