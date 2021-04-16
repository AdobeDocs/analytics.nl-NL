---
description: Stappen die beschrijven hoe u gegevensbestanden kunt uploaden via FTP.
subtopic: Classifications
title: FTP-import
feature: Admin Tools
uuid: a914970d-ba02-4111-9dcf-06448f71b9f3
exl-id: 3e93b35c-6f65-4a93-887d-d94e4d359bdc
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 2%

---

# FTP-import

Stappen die beschrijven hoe u gegevensbestanden kunt uploaden via FTP.

## FTP-import {#concept_2F965BE873254546A61FB755F25299FD}

Stappen die beschrijven hoe u gegevensbestanden kunt uploaden via FTP.

**[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

De volgende aanbevolen limieten zijn belangrijk:

* Veel kleine bestanden leiden tot een langzamere verwerking dan een paar grote bestanden. Dit is toe te schrijven aan de hoeveelheid het een rij vormen en het voorrang geven vereist voor de kleinere banen.
* Breek grote bestanden uit in 50 MB blokken. Dit is niet nodig, maar wordt aanbevolen omdat het achterste gedeelte beter zichtbaar wordt. Ook, als de fouten voorkomen terwijl wij uw baan verwerken, zal de baan opnieuw beginnen; grote bestanden resulteren in grote hoeveelheden werk opnieuw.

De eerste setup vult de classificatiedatabase met een grote set oorspronkelijke gegevens, of herstructureert de classificaties in plaats van een paar rijen opnieuw te classificeren of rijen toe te voegen.

Na een eerste upload in een rapportsuite (voor een bepaalde variabele of rapport), raadt Adobe aan alleen nieuwe en bijgewerkte rijen te uploaden in volgende importbewerkingen. Rijen die niet worden gewijzigd, moeten worden weggelaten uit toekomstige uploads.

Elke nieuwe sleutelwaarde die u uploadt, telt mee voor uw unieke waarden voor die variabele voor de maand.

Als u uw uniques voor de maand hebt overschreden, zult u de overeenkomstige classificatiegegevens voor de uniques niet zien overschrijden waarden in rapportering. Je kunt die classificaties in de Data Warehouse zien.

>[!NOTE]
>
>De tijd die nodig is om een bestand met classificatiegegevens te verwerken, is afhankelijk van de grootte van het bestand en het huidige aantal bestanden dat al wordt verwerkt door Adobe. De verwerking van gegevensbestanden duurt gewoonlijk niet langer dan 72 uur.

Maak een FTP-account voordat u gegevens uploadt via FTP. Zie [Een FTP-account maken](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF) voor meer informatie.

## Classificaties importeren via FTP {#task_132C36830B69418B8C929E39838EF01D}

<!-- 

t_upload_a_saint_data_file_via_ftp.xml

 -->

Stappen die beschrijven hoe u een FTP-account kunt gebruiken om classificaties te importeren in Adobe Analytics.

Zie [Een FTP-account maken](/help/components/classifications/importer/c-uploading-saint-data-files-via-ftp.md#task_C019268E6C934C7C95F4326F42A22CCF) voor meer informatie over het maken van een FTP-account.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klik **[!UICONTROL Import File]**, dan klik **[!UICONTROL FTP Import]**.
1. Klik op **[!UICONTROL View]** naast de FTP-account die u wilt gebruiken.
1. Gebruik de FTP-toegangsgegevens (Host, Aanmelden, Wachtwoord) om toegang te krijgen tot de FTP-server via een door u gekozen FTP-client.
1. Upload het gegevensbestand ( [!DNL .tab] of [!DNL .txt]) aan de server van FTP.
1. Na het uploaden van het gegevensbestand, upload een FIN dossier dat erop wijst het dossier klaar is te verwerken.

   Het FIN-bestand is een leeg bestand met dezelfde naam als het gegevensbestand, met de bestandsnaamextensie [!DNL .fin]. Als uw gegevensbestand bijvoorbeeld [!DNL classdata1.tab] is, is de bestandsnaam FIN [!DNL classdata1.fin].

Met regelmatige intervallen haalt Adobe geüploade gegevensbestanden op waaraan een FIN-bestand is gekoppeld. Adobe importeert ze in de rapportsuite en gegevenssets die zijn opgegeven in de FTP-accountconfiguratie.

## Een FTP-account maken {#task_C019268E6C934C7C95F4326F42A22CCF}

Maak een FTP-account voordat u gegevens uploadt via FTP. >

<!-- 

t_create_an_ftp_account.xml

 -->

Zie [FTP en sFTP](https://docs.adobe.com/content/help/en/analytics/export/ftp-and-sftp/ftp-overview.html) voor meer informatie over Adobe FTP-servers.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klik **[!UICONTROL Import File]**, dan klik **[!UICONTROL FTP Import]**.
1. Klik op het tabblad **[!UICONTROL Import File]** op **[!UICONTROL Add New]**.
1. Geef de FTP-accountgegevens op:

   | Element | Beschrijving |
   |---|---|
   | Naam | De naam van de FTP-account. |
   | Te classificeren gegevensset | Selecteer in de vervolgkeuzelijst de gegevensset (variabele marketingrapport) die u wilt classificeren. |
   | Rapportsets selecteren | Selecteer de rapportsuites waar u de geselecteerde gegevensreeks wilt classificeren. Om veelvoudige rapportreeksen te selecteren, moeten de classificaties voor elk van de geselecteerde rapportreeksen identiek zijn. |
   | Gegevens bij conflicten overschrijven | Selecteer deze optie als u dubbele gegevens wilt overschrijven. Deze optie is handig als u bestaande classificaties bijwerkt. Als u aanvullende classificaties toevoegt, wordt deze optie niet aanbevolen. |
   | Na importeren is voltooid | Selecteer deze optie als u de bijgewerkte gegevensset automatisch wilt exporteren naar dezelfde FTP-account als u het e-mailadres opgeeft voor de ontvangst van meldingen over deze FTP-account nadat het importeren is voltooid. |
   | Ontvanger van kennisgeving | Geef het e-mailadres op waar meldingen over dit FTP-account moeten worden ontvangen. |
   | Autoriseren | (Vereist) Hiermee geeft u Adobe toestemming om automatisch alle gegevensbestanden te importeren die naar het nieuwe FTP-account zijn verzonden. |

1. Klik op **[!UICONTROL Save]**.

Als u een FTP-account hebt gemaakt, kunt u deze bewerken of verwijderen door op de desbetreffende koppeling naast de gewenste FTP-account te klikken.

>[!NOTE]
>
>Meldingen worden niet verzonden als bij het importeren geen wijzigingen in een classificatie worden aangebracht. Een e-mailbericht wordt alleen verzonden als dit is gelukt en leidt tot wijzigingen in een classificatie.
