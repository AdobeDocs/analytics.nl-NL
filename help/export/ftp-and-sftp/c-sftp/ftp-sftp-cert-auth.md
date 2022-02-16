---
description: Verbinding maken zonder wachtwoord met FTP-accounts is alleen mogelijk met zowel een SFTP-verbinding als een alternatieve verificatiemethode. Dit omvat een reeks van twee dossiers (één om op de rekening van FTP te verblijven en andere om op uw computer te verblijven) genoemd een openbare en privé zeer belangrijke combinatie.
keywords: ftp;sftp
title: Verbinding maken met Adobe via SFTP zonder wachtwoord
feature: FTP Export
exl-id: 7ff9511c-50a2-466f-b5af-6bbd59941ce5
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 2%

---

# Verbinding maken met Adobe via SFTP zonder wachtwoord

Verbinding maken zonder wachtwoord met FTP-accounts is alleen mogelijk met zowel een SFTP-verbinding als een alternatieve verificatiemethode. Dit omvat een reeks van twee dossiers (één om op de rekening van FTP te verblijven en andere om op uw computer te verblijven) genoemd een openbare en privé zeer belangrijke combinatie.

Dit is niet minder veilig dan wachtwoordverificatie. Het is een andere vorm van het voor authentiek verklaren die niet de gebruiker vereist om een wachtwoord in te typen telkens. Als deze bestanden correct worden gebruikt, kan de computer zich aanmelden zonder dat een wachtwoord hoeft te worden opgegeven. Dit moet per computer worden ingesteld. Alle andere verbindingen die deze zeer belangrijke dossiers niet gebruiken moeten nog een wachtwoord specificeren.

SFTP (Secure File Transfer Protocol) wordt vereist door sommige clients voor het verzenden van vertrouwelijke gegevens. Een SFTP-verbinding is veiliger dan een normale FTP-verbinding omdat gecodeerde gegevenscommunicatie hierdoor mogelijk is. Standaard zijn alle Adobe FTP-accounts gereed voor SFTP. Een verbinding SFTP kan met een geldige gebruikersbenaming en een wachtwoord worden geopend door een cliënt van SFTP te gebruiken die op haven 22 (normale verbindingen van FTP verbindt die niet-veilige gebruikshaven 21 zijn).

Als u SFTP gebruikt, is het mogelijk om onder specifieke omstandigheden persoonlijke sleutels te gebruiken om zonder wachtwoord verbinding te maken met de account. Met deze methode kan de computer sleutelbestanden gebruiken voor verificatie in plaats van gebruikelijke wachtwoordverificatie. Dit betekent dat alleen de computer met de persoonlijke sleutel verbinding kan maken zonder wachtwoord. Alle andere computers/gebruikers moeten nog wachtwoordauthentificatie gebruiken (tenzij de privé sleutels opstelling ook op deze andere computers zijn).

**Persoonlijke sleutels instellen en gebruiken voor verificatie zonder wachtwoord**

1. FTP-account gemaakt (Adobe).

   Een Adobe-medewerker kan een FTP-account maken als dat nog niet het geval is. Neem contact op met uw Adobe-accountmanager of de klantenservice van Adobe om een account te maken.
1. Openbare/persoonlijke sleutel maken (klant).

   Een combinatie van openbare en persoonlijke sleutels maken. De persoonlijke sleutel is een bestand dat privé is met uw computer/server en zich daar bevindt. Het bestand met de openbare sleutel moet worden geüpload naar de Adobe-account. Wanneer gebruikt op deze manier kunt u verbinding maken zonder wachtwoordverificatie. Het bestand met de openbare sleutel bij Adobe komt overeen met het bestand met de persoonlijke sleutel op uw computer/server en wordt op die manier geverifieerd.

   Om deze dossiers tot stand te brengen, contacteer uw interne groep van de netwerksteun om een zeer belangrijke reeks tot stand te brengen die voor uw milieu behoorlijk is. Er zijn vele hulpmiddelen en toepassingen die kunnen worden gebruikt om deze twee dossiers tot stand te brengen.

   Een voorbeeld van hoe dit in een shell van UNIX milieu kan worden gedaan wordt getoond hieronder. Dit is slechts één voorbeeld van hoe dit kan worden gedaan en dient als nuttig referentiepunt voor het communiceren van vereisten aan uw team of interne netwerkgroep.

   ```
   // Linux/Unix (bash shell)
   
   // First make sure the ".ssh" directory exists
   
   $ mkdir ~/.ssh
   
   $ cd ~/.ssh
   
   // Now actually generate the key pair
   
   // Usually we will want to create an empty passphrase (just hit "Enter" for both password prompts)
   
   $ ssh-keygen -q -t dsa
   
   Enter file in which to save the key (/home/user/.ssh/id_dsa):
   
   Enter passphrase (empty for no passphrase): ...
   
   Enter same passphrase again: ...
   
   // Rename or copy the public key file to "authorized_keys"
   
   // This "authorized_keys" file is the one that we will upload to the Adobe FTP server in step 3
   
   $ cp id_dsa.pub authorized_keys 
   ```

1. Upload Public key naar FTP-account (klant).

   Upload en test de openbare sleutel. Maak verbinding met de Adobe FTP-account en maak een [!DNL .ssh] directory, als deze nog niet bestaat. Upload de [!DNL authorized_keys] bestand naar dit bestand [!DNL .ssh] directory. Dit kan op verschillende manieren worden gedaan (opdrachtregel, grafische FTP-client, enzovoort). Het enige wat nodig is, is de mogelijkheid om een map te maken en een bestand te uploaden.

   Hier, opnieuw, is een voorbeeld van het doen van dit gebruikend een shell van UNIX.

   ```
   $ ftp ftp.Adobe.com
   
   OR (depending on hostname provided by Adobe)
   
   $ ftp ftp2.Adobe.com
   
   // Enter username and password for account as prompted
   
   ftp> mkdir .ssh
   
   ftp> cd .ssh
   
   ftp> put authorized_keys
   
   ftp> exit
   
   // Now test the connection by logging in to the server using "sftp" command:
   
   $ sftp username@ftp.omniture.com
   
   OR (depending on hostname provided by Adobe)
   
   $ sftp username@ftp2.omniture.com
   
   // You should immediately receive an sftp prompt without having to enter the password:
   
   sftp>
   ```
