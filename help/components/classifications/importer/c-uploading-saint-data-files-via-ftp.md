---
description: Gegevensbestanden uploaden via FTP.
title: FTP-import
feature: Classifications
exl-id: 3e93b35c-6f65-4a93-887d-d94e4d359bdc
source-git-commit: c36cc9884b2de3cddf03b505d9c4883dcac846af
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 1%

---

# FTP-import

>[!IMPORTANT]
>
>We raden u niet meer aan FTP te gebruiken voor importeren, zoals op deze pagina wordt beschreven.
>
>FTP wordt niet aanbevolen omdat het een niet-gecodeerde methode is voor het delen van bestanden, wat betekent dat iedereen de bestandsinhoud en de gebruikersnaam en het wachtwoord voor de account kan onderscheppen.
>
>In plaats daarvan configureert u een cloudaccount zoals beschreven in [Cloudimportlocaties configureren](/help/components/classifications/importer/configure-import-accounts.md).

Stappen die beschrijven hoe u gegevensbestanden kunt uploaden via FTP.

## FTP-import {#concept_2F965BE873254546A61FB755F25299FD}

Gegevensbestanden uploaden via FTP:

1. **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.

De volgende aanbevolen limieten zijn belangrijk.

>[!IMPORTANT]
>
>Als u te veel kleine of grote bestanden hebt, kan de verwerking op de verwerkingsservers onnodig worden belast. Adobe raadt aan grote bestanden op te splitsen in 50 MB blokken en kleine bestanden samen te voegen.

De eerste setup vult de classificatiedatabase met een grote set oorspronkelijke gegevens, of herstructureert de classificaties in plaats van een paar rijen opnieuw te classificeren of rijen toe te voegen.

Na een eerste upload in een rapportsuite (voor een bepaalde variabele of rapport), raadt Adobe aan alleen nieuwe en bijgewerkte rijen te uploaden in volgende importbewerkingen. Rijen die niet worden gewijzigd, moeten worden weggelaten uit toekomstige uploads.

Elke nieuwe sleutelwaarde die u uploadt, telt mee voor uw unieke waarden voor die variabele voor de maand.

Als u uw uniques voor de maand hebt overschreden, zult u de overeenkomstige classificatiegegevens voor de uniques niet zien overschrijden waarden in rapportering. Je kunt die classificaties in de Data Warehouse zien.

>[!NOTE]
>
>De tijd die nodig is om een bestand met classificatiegegevens te verwerken, is afhankelijk van de grootte van het bestand en het huidige aantal bestanden dat al wordt verwerkt door Adobe. De verwerking van gegevensbestanden duurt gewoonlijk niet langer dan 72 uur.

## Een FTP-account maken

Maak een FTP-account voordat u gegevens uploadt via FTP. >

Zie [FTP en sFTP](/help/export/ftp-and-sftp/ftp-overview.md) voor meer informatie over Adobe FTP-servers.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klikken **[!UICONTROL Import File]** en klik vervolgens op **[!UICONTROL FTP Import]**.
1. Op de **[!UICONTROL Import File]** tabblad, klikt u op **[!UICONTROL Add New]**.
1. Geef de FTP-accountgegevens op:

   | Element | Beschrijving |
   |---|---|
   | **Naam** | De naam van de FTP-account. |
   | **Te classificeren gegevensset** | Selecteer in de vervolgkeuzelijst de gegevensset (variabele marketingrapport) die u wilt classificeren. |
   | **Rapportsets selecteren** | Selecteer de rapportsuites waar u de geselecteerde gegevensreeks wilt classificeren. Om veelvoudige rapportreeksen te selecteren, moeten de classificaties voor elk van de geselecteerde rapportreeksen identiek zijn. |
   | **Gegevens bij conflicten overschrijven** | Selecteer deze optie als u dubbele gegevens wilt overschrijven. Deze optie is handig als u bestaande classificaties bijwerkt. Als u op de [nieuwste classificatiearchitectuur](../sets/overview.md)Deze instelling is altijd ingeschakeld. |
   | **Na importeren is voltooid** | Selecteer deze optie als u de bijgewerkte gegevensset automatisch wilt exporteren naar dezelfde FTP-account als u het e-mailadres opgeeft voor de ontvangst van meldingen over deze FTP-account nadat het importeren is voltooid. Als u op de [nieuwste classificatiearchitectuur](../sets/overview.md), is deze optie niet beschikbaar. |
   | **Ontvanger van kennisgeving** | Geef het e-mailadres op waar meldingen over dit FTP-account moeten worden ontvangen. |
   | **Autoriseren** | (Vereist) Hiermee geeft u Adobe toestemming om automatisch alle gegevensbestanden te importeren die naar het nieuwe FTP-account zijn verzonden. |

1. Klik op **[!UICONTROL Save]**.

Als u een FTP-account hebt gemaakt, kunt u deze bewerken of verwijderen door op de desbetreffende koppeling naast de gewenste FTP-account te klikken.

>[!NOTE]
>
>Meldingen worden niet verzonden als bij het importeren geen wijzigingen in een classificatie worden aangebracht. Een e-mailbericht wordt alleen verzonden als dit is gelukt en leidt tot wijzigingen in een classificatie.

## Classificaties importeren via FTP

U kunt een FTP-account gebruiken om classificaties te importeren in Adobe Analytics.

Classificaties importeren via FTP:

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klikken **[!UICONTROL Import File]** en klik vervolgens op **[!UICONTROL FTP Import]**.
1. Klik naast de FTP-account die u wilt gebruiken op **[!UICONTROL View]**.
1. Gebruik de FTP-toegangsgegevens (Host, Aanmelden, Wachtwoord) om toegang te krijgen tot de FTP-server via een door u gekozen FTP-client.
1. Het gegevensbestand uploaden ( `.tab` of `.txt`) naar de FTP-server.
1. Na het uploaden van het gegevensbestand, upload een FIN dossier dat erop wijst het dossier klaar is te verwerken.

   Het FIN-bestand is een leeg bestand met dezelfde naam als het gegevensbestand, met een `.fin` bestandsnaamextensie. Als het gegevensbestand bijvoorbeeld `classdata1.tab`, de FIN-bestandsnaam is `classdata1.fin`.

Met regelmatige intervallen haalt Adobe geüploade gegevensbestanden op waaraan een FIN-bestand is gekoppeld. Adobe importeert ze in de rapportsuite en gegevenssets die zijn opgegeven in de FTP-accountconfiguratie.

Nadat Adobe Analytics bestanden heeft gelezen en verwerkt die in de FTP-map zijn geüpload, worden de bestanden automatisch van de FTP-site verwijderd.
