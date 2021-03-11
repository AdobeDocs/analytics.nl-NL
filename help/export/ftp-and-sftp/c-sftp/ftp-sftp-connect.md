---
description: Instructies voor het instellen van een beveiligde overdracht met Adobe FTP-servers.
keywords: ftp;sftp
title: Verbinding maken met een Adobe FTP-account met SFTP
uuid: 4faf27b8-7276-4c68-87cb-35802b809e27
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 11%

---


# Verbinding maken met een Adobe FTP-account met SFTP

Instructies voor het instellen van een beveiligde overdracht met Adobe FTP-servers.

1. Vraag een door Adobe gehoste FTP-account (50 MB quota) aan.
1. Maak openbare/persoonlijke RSA-sleutels. Voer in Linux de volgende handelingen uit:

   ```
   ssh-keygen -t rsa
   ```

   Als u in een milieu van Vensters bent, gebruik puttyGen om de sleutels tot stand te brengen.

1. Maak een bestand met de naam [!DNL authorized_keys] (geen extensie).
1. Kopieer de inhoud van de openbare sleutel naar [!DNL authorized_keys].
1. [!DNL authorized_keys] uploaden naar een FTP-account:

   * Maak verbinding met de Adobe FTP-account.
   * Maak een map [!DNL .ssh] (als deze nog niet bestaat).
   * Upload het [!DNL authorized_keys] dossier aan [!DNL .ssh] folder.

1. Test de verbinding door u met SFTP aan te melden bij de FTP-account.

Zie [Verbinding maken met Adobe via sFTP zonder wachtwoord_ voor meer informatie.](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).
