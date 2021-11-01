---
title: Problemen met gegevensfeeds oplossen
description: Leer hoe u problemen kunt vaststellen en oplossen met Gegevensfeeds.
keywords: taak;problemen oplossen;fout;ftp;chdir;connect;login;put
exl-id: c082bc95-cdae-448b-86b5-695660fb2352
source-git-commit: b81ffba2f1e021888dd1c4b016c9b451448f47bb
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Gegevensfeeds oplossen

Bepaal potentiële redenen waarom een baan zou kunnen er niet in slagen om te verwerken of te leveren.

## Een bestaande gegevensfeed oplossen

Als u een gegevensfeed hebt die per uur of per dag werkt maar onlangs mislukt, controleert u elk van de volgende opties:

* Gebruik de [Adobe-status, gereedschap](https://status.adobe.com/en/experience_cloud) om te bepalen of er om het even welke geplande onderhoudsvensters of beschikbaarheidskwesties zijn. Als er een bekende kwestie op dat moment is, verwerkt Adobe automatisch geplande gegevensvoer zodra de dienst wordt hersteld.
* Controleer of er voldoende ruimte beschikbaar is op de FTP-site. Als er onvoldoende schijfruimte beschikbaar is voor de FTP-site, verwijdert u enkele bestanden van de server om ruimte vrij te maken voor nieuwe bestanden.
* Als er geen bekende problemen zijn en de FTP-site over voldoende schijfruimte beschikt, kunt u de gegevensfeed opnieuw verzenden.

   1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Data feeds]**.
   2. Zoek de gewenste gegevensinvoer(s) en klik vervolgens op het selectievakje naast elke feed die u opnieuw wilt uitvoeren.
   3. Klik op **[!UICONTROL Rerun]**.

   ![Rerun](assets/rerun.png)

Neem contact op met de klantenservice als u de bestanden met de gegevensinvoer nog steeds niet ontvangt nadat u deze opnieuw hebt uitgevoerd.

## Een nieuwe gegevensfeed oplossen

Als een nieuwe gegevensvoer een fout veroorzaakt, los de kwestie door een testdossier aan de plaats van FTP manueel te uploaden problemen op. In de meeste gevallen kunt u met deze stappen bepalen waar de fout optreedt.

1. Meld u aan bij uw FTP-site met Bestandverkenner (Windows) of Finder (Mac). Controleer of u FTP-protocol (`ftp://`) en die u toestaat [Adobe](/help/technotes/ip-addresses.md) via de firewall van uw organisatie. Als u de FTP-site niet kunt bereiken, werkt u samen met de eigenaar van de FTP-site om de juiste bestemming te bepalen.

   ![Bestandsverkenner](assets/file_explorer.png)

2. Er wordt een pop-up weergegeven met de vraag naar een gebruikersnaam en wachtwoord. Voer uw verificatiereferenties in. Als de referenties worden geaccepteerd, wordt in het venster de huidige inhoud op de FTP-site weergegeven. Als de referenties niet worden geaccepteerd, werkt u samen met de FTP-eigenaar om te controleren of de gebruikersnaam en het wachtwoord correct zijn. Als u SFTP gebruikt, moet u elke stap in het dialoogvenster [SFTP-handleiding](../ftp-and-sftp/c-sftp/ftp-sftp.md). Merk op dat Adobe niet alle SFTP gebruiksgevallen steunt.
3. Upload een bestand naar de FTP-site door het naar het geverifieerde venster te slepen. Een afbeelding of tekstdocument is geschikt. Als er een fout optreedt bij het plaatsen van een bestand op de FTP-site, werkt u samen met de FTP-eigenaar om te controleren of er voldoende schijfruimte is en of de gebruikersnaam schrijfmachtigingen voor de FTP-site heeft.
4. Nadat u hebt bevestigd dat het bestand zich op de FTP-site bevindt, kunt u het bestand verwijderen dat in de vorige stap is geüpload.

Als alle bovenstaande stappen werken en u nog steeds een FTP-fout krijgt, neemt u contact op met de klantenservice.
