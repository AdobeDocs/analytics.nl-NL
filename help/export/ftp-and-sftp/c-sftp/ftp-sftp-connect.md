---
description: Instructies voor het instellen van een beveiligde overdracht met Adobe FTP-servers.
keywords: ftp;sftp
title: Verbinding maken met een Adobe FTP-account met SFTP
feature: FTP Export
exl-id: 727d4f7a-d7d1-40cf-bdcd-c783ca47f51c
source-git-commit: 62132284ca70f3bdb1a8896e4548b8b63a5c03c8
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---

# Verbinding maken met een FTP-account met SFTP

Beveiligde overdracht instellen met FTP:

1. (Voorwaardelijk) Als u beveiligde overdracht wilt instellen met Adobe FTP-servers:

   1. Vraag een door Adobe gehoste FTP-account (50 MB quota) aan.

   1. Maak openbare/persoonlijke RSA-sleutels.

      * Voer in Linux-omgeving de volgende handelingen uit:

        ```
        ssh-keygen -t rsa
        ```

      * Gebruik puttyGen in een Windows-omgeving.

1. (Voorwaardelijk) als u veilige overdracht met uw eigen plaats van FTP wilt opstelling, moet u een gastheer SFTP, een gebruikersbenaming, en de bestemmingsplaats hebben die een geldige RSA of DSA openbare sleutel bevatten. U kunt de juiste openbare sleutel downloaden wanneer u de feed maakt.

1. Een bestand met de naam [!DNL authorized_keys] (geen extensie).

1. Inhoud van openbare sleutel kopiëren naar [!DNL authorized_keys].

1. Uploaden [!DNL authorized_keys] naar een FTP-account:

   * Maak verbinding met de Adobe FTP-account.
   * Een [!DNL .ssh] directory (als deze nog niet bestaat).
   * Upload de [!DNL authorized_keys] aan de [!DNL .ssh] directory.

1. Test de verbinding door u met SFTP aan te melden bij de FTP-account.

Voor meer gedetailleerde informatie, zie [Hoe te om met Adobe via sFTP zonder een Wachtwoord te verbinden...](/help/export/ftp-and-sftp/c-sftp/ftp-sftp-cert-auth.md).
