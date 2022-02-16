---
description: Instructies voor het instellen van een beveiligde overdracht met Adobe FTP-servers.
keywords: ftp;sftp
title: Verbinding maken met een Adobe FTP-account met SFTP
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
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

1. Een bestand met de naam [!DNL authorized_keys] (geen extensie).
1. De inhoud van de openbare sleutel kopiëren naar [!DNL authorized_keys].
1. Uploaden [!DNL authorized_keys] naar een FTP-account:

   * Maak verbinding met de Adobe FTP-account.
   * Een [!DNL .ssh] directory (als deze nog niet bestaat).
   * Upload de [!DNL authorized_keys] aan de [!DNL .ssh] directory.

1. Test de verbinding door u met SFTP aan te melden bij de FTP-account.

Zie voor meer informatie [Hoe te om met Adobe via sFTP zonder een Wachtwoord te verbinden...](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).
