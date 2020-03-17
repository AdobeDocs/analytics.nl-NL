---
description: Instructies voor het instellen van een veilige overdracht met Adobe FTP-servers.
keywords: ftp;sftp
title: Verbinding maken met een Adobe FTP-account met SFTP
uuid: 4faf27b8-7276-4c68-87cb-35802b809e27
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Verbinding maken met een Adobe FTP-account met SFTP

Instructies voor het instellen van een veilige overdracht met Adobe FTP-servers.

1. Een door Adobe gehoste FTP-account aanvragen (50 MB quota).
1. Maak openbare/persoonlijke RSA-sleutels. Voer in Linux de volgende handelingen uit:

   ```
   ssh-keygen -t rsa
   ```

   Als u in een milieu van Vensters bent, gebruik puttyGen om de sleutels tot stand te brengen.

1. Maak een bestand met de naam [!DNL authorized_keys] (geen extensie).
1. Kopieer de inhoud van de openbare sleutel in [!DNL authorized_keys].
1. Uploaden [!DNL authorized_keys] naar een FTP-account:

   * Maak verbinding met de Adobe FTP-account.
   * Maak een [!DNL .ssh] map (als deze nog niet bestaat).
   * Upload het [!DNL authorized_keys] bestand naar de [!DNL .ssh] map.

1. Test de verbinding door u met SFTP aan te melden bij de FTP-account.

Zie [Verbinding maken met Adobe via sFTP zonder wachtwoord_ voor meer informatie...](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).
