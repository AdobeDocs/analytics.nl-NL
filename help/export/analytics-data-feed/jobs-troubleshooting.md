---
description: Als er een fout optreedt, wordt er een fout gerapporteerd in de kolom Taakstatus.
keywords: Data Feed;job;troubleshooting;error;ftp;chdir;connect;login;put
title: Taken oplossen
uuid: 8fbb914e-03db-434e-b4d3-8594144ff2b7
translation-type: tm+mt
source-git-commit: ''

---


# Taken oplossen

Als u problemen ondervindt bij het weergeven van een gegevensfeed op uw FTP-site, gebruikt u deze pagina om te begrijpen waarom.

## Foutcodes

Als er een fout optreedt, wordt er een fout gerapporteerd in de kolom Taakstatus.

### FTP-chdir-fout

De feed kan niet naar de opgegeven map navigeren of schrijven. Controleer of de doelmap op de FTP-site aanwezig is en of de gegevens in de opgegeven map de juiste lees-/schrijfmachtigingen hebben.

### FTP Connect-fout

De feed kan geen verbinding maken met de FTP-bestemming. Controleer of de FTP-bestemming correct en geldig is.

### FTP-fout

Een algemene fout waarbij de feed het bestand uiteindelijk niet naar de FTP-site kan schrijven. Deze fout kan mogelijk ontstaan als de schijf van de FTP-server vol is of als de quota is overschreden. De fout kan ook afkomstig zijn van een netwerk- of doelserverfout.

### FTP-aanmeldfout

De feed kan zich niet aanmelden met de opgegeven referenties. Controleer of de gebruikersnaam en het wachtwoord voor FTP correct zijn.

### FTP-plaatsingsfout

De feed kan geen bestanden naar de FTP-site schrijven. Controleer of de FTP-aanmelding de juiste machtigingen heeft voor het lezen en schrijven van gegevens op uw FTP-site. Deze fout kan ook mogelijk afkomstig zijn van een volledige schijf of een overschrijding van de schijfquota op de FTP-server.

## Stappen om problemen op te lossen

Meld u aan bij uw FTP-site en upload bestanden naar deze site. In de meeste gevallen kunt u met deze stappen bepalen waar de fout optreedt.

1. Meld u aan bij uw FTP-site met Bestandverkenner (Windows) of Finder (Mac). Gebruik FTP-protocol (`ftp://`). Als u de FTP-site niet kunt bereiken, kunt u met de eigenaar van de FTP-site bepalen wat de juiste bestemming is.

   ![Bestandsverkenner](assets/file_explorer.png)

2. Er wordt een pop-up weergegeven met de vraag naar een gebruikersnaam en wachtwoord. Voer uw verificatiereferenties in. Als de referenties worden geaccepteerd, wordt in het venster de huidige inhoud op de FTP-site weergegeven. Als de referenties niet worden geaccepteerd, kunt u met de FTP-eigenaar werken om ervoor te zorgen dat de gebruikersnaam en het wachtwoord correct zijn.
3. Upload een bestand naar de FTP-site door het naar het geverifieerde venster te slepen. Een afbeelding of tekstdocument is geschikt. Als er een fout optreedt bij het plaatsen van een bestand op de FTP-site, werkt u samen met de FTP-eigenaar om te controleren of er voldoende schijfruimte is en of de gebruikersnaam schrijfmachtigingen voor de FTP-site heeft.
4. Nadat u hebt bevestigd dat het bestand zich op de FTP-site bevindt, kunt u het bestand verwijderen dat in de vorige stap is geüpload.
5. Als alle bovenstaande stappen werken en u nog steeds een FTP-fout krijgt, kunt u contact opnemen met de klantenondersteuning.
