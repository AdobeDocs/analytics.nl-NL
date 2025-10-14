---
description: Gegevensbestanden uploaden via FTP.
title: FTP importeren
feature: Classifications
exl-id: 3e93b35c-6f65-4a93-887d-d94e4d359bdc
source-git-commit: 4eea524bf95c9b6bc9ddc878c8c433bc1e60daee
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 0%

---

# FTP-import (verouderd)

{{classification-importer-deprecation}}

>[!IMPORTANT]
>
>Adobe raadt niet langer aan FTP te gebruiken voor importeren zoals op deze pagina wordt beschreven.
>
>FTP wordt niet aanbevolen omdat het een niet-gecodeerde methode is voor het delen van bestanden, wat betekent dat iedereen de bestandsinhoud en de gebruikersnaam en het wachtwoord voor de account kan onderscheppen.
>
>In plaats daarvan, vorm een wolkenrekening zoals die in [&#x200B; wordt beschreven cloudinvoer en uitvoerrekeningen &#x200B;](/help/components/locations/configure-import-accounts.md) vormt.

Stappen die beschrijven hoe u gegevensbestanden kunt uploaden via FTP.

## FTP importeren {#concept_2F965BE873254546A61FB755F25299FD}

Gegevensbestanden uploaden via FTP:

1. **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]** .

De volgende aanbevolen limieten zijn belangrijk.

>[!IMPORTANT]
>
>Als u te veel kleine of grote bestanden hebt, kan de verwerking op de verwerkingsservers onnodig worden belast. Adobe raadt aan grote bestanden op te splitsen in 50 MB blokken en kleine bestanden samen te voegen.

De eerste setup vult de classificatiedatabase met een grote set oorspronkelijke gegevens, of herstructureert de classificaties in plaats van een paar rijen opnieuw te classificeren of rijen toe te voegen.

Na een eerste upload in een rapportsuite (voor een bepaalde variabele of rapport) raadt Adobe aan alleen nieuwe en bijgewerkte rijen te uploaden in volgende importbewerkingen. Rijen die niet worden gewijzigd, moeten worden weggelaten uit toekomstige uploads.

Elke nieuwe sleutelwaarde die u uploadt, telt mee voor uw unieke waarden voor die variabele voor de maand.

Als u uw uniques voor de maand hebt overschreden, zult u de overeenkomstige classificatiegegevens voor de uniques niet zien overschrijden waarden in rapportering. Je kunt die classificaties zien in Data Warehouse.

>[!NOTE]
>
>De tijd die nodig is om een bestand met classificatiegegevens te verwerken, is afhankelijk van de grootte van het bestand en het huidige aantal bestanden dat al door Adobe-servers wordt verwerkt. De verwerking van gegevensbestanden duurt gewoonlijk niet langer dan 72 uur.

## Een FTP-account maken

Maak een FTP-account voordat u gegevens uploadt via FTP. >

Zie [&#x200B; FTP en sFTP &#x200B;](/help/export/ftp-and-sftp/ftp-overview.md) voor extra details op de servers van FTP van Adobe.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]** .
1. Klik op **[!UICONTROL Import File]** en vervolgens op **[!UICONTROL FTP Import]** .
1. Klik op het tabblad **[!UICONTROL Import File]** op **[!UICONTROL Add New]** .
1. Geef de FTP-accountgegevens op:

   | Element | Beschrijving |
   |---|---|
   | **Naam** | De naam van de FTP-account. |
   | **Te classificeren Reeks van Gegevens** | Selecteer in de vervolgkeuzelijst de gegevensset (variabele marketingrapport) die u wilt classificeren. |
   | **Uitgezochte de Reeksen van het Rapport** | Selecteer de rapportsuites waar u de geselecteerde gegevensreeks wilt classificeren. Om veelvoudige rapportreeksen te selecteren, moeten de classificaties voor elk van de geselecteerde rapportreeksen identiek zijn. |
   | **beschrijven Gegevens over Conflicten** | Selecteer deze optie als u dubbele gegevens wilt overschrijven. Deze optie is handig als u bestaande classificaties bijwerkt. Als u op de [&#x200B; recentste classificatiearchitectuur &#x200B;](../sets/overview.md) bent, wordt dit het plaatsen altijd toegelaten. |
   | **na de Invoer is Volledig** | Selecteer deze optie als u de bijgewerkte gegevensset automatisch wilt exporteren naar dezelfde FTP-account als u het e-mailadres opgeeft voor de ontvangst van meldingen over deze FTP-account nadat het importeren is voltooid. Als u op de [&#x200B; recentste classificatiearchitectuur &#x200B;](../sets/overview.md) bent, is deze optie niet beschikbaar. |
   | **Ontvanger van het Bericht** | Geef het e-mailadres op waar meldingen over dit FTP-account moeten worden ontvangen. |
   | **machtigt** | (Vereist) Hiermee geeft u Adobe toestemming om automatisch alle gegevensbestanden te importeren die naar het nieuwe FTP-account zijn verzonden. |

1. Klik op **[!UICONTROL Save]**.

Als u een FTP-account hebt gemaakt, kunt u deze bewerken of verwijderen door op de desbetreffende koppeling naast de gewenste FTP-account te klikken.

>[!NOTE]
>
>Meldingen worden niet verzonden als bij het importeren geen wijzigingen in een classificatie worden aangebracht. Een e-mailbericht wordt alleen verzonden als dit is gelukt en leidt tot wijzigingen in een classificatie.

## Classificaties importeren via FTP

U kunt een FTP-account gebruiken om classificaties te importeren in Adobe Analytics.

Classificaties importeren via FTP:

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]** .
1. Klik op **[!UICONTROL Import File]** en vervolgens op **[!UICONTROL FTP Import]** .
1. Klik op **[!UICONTROL View]** naast de FTP-account die u wilt gebruiken.
1. Gebruik de FTP-toegangsgegevens (Host, Aanmelden, Wachtwoord) om toegang te krijgen tot de FTP-server via een door u gekozen FTP-client.
1. Upload het gegevensbestand ( `.tab` of `.txt` ) naar de FTP-server.
1. Na het uploaden van het gegevensbestand, upload een FIN dossier dat erop wijst het dossier klaar is te verwerken.

   Het FIN-bestand is een leeg bestand met dezelfde naam als het gegevensbestand, met de bestandsnaamextensie `.fin` . Als het gegevensbestand bijvoorbeeld `classdata1.tab` is, is de bestandsnaam FIN `classdata1.fin` .

Met regelmatige tussenpozen haalt Adobe geüploade gegevensbestanden op waaraan een FIN-bestand is gekoppeld. Adobe importeert deze naar de rapportensuites en gegevenssets die zijn opgegeven in de configuratie van de FTP-account.

Nadat Adobe Analytics bestanden heeft gelezen en verwerkt die in de FTP-map zijn geüpload, worden de bestanden automatisch van de FTP-site verwijderd.
