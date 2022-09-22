---
title: Upgrade van SFTP-services - Veelgestelde vragen
description: Veelgestelde vragen over de geplande SFTP-services-upgrade.
feature: FTP Export
exl-id: e271b545-0769-4a69-9d7f-dc46bc654737
source-git-commit: 70ede981a0f6f7aebbbdf4dbcbf9e5187a3df495
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Upgrade van SFTP-services - Veelgestelde vragen

In september 2022 zal Adobe Analytics zijn Secure File Transfer Protocol bijwerken [SFTP] om de beveiliging van bestandsoverdrachten te verbeteren. Door deze wijziging worden sommige SFTP-clientconfiguraties niet meer ondersteund. Dit is alleen van invloed op gegevens die via SFTP naar Adobe Analytics worden verzonden of van worden opgehaald. Het FTP-protocol wordt niet beïnvloed. Om onderbreking van de dienst te vermijden, gelieve uw cliënten SFTP (code, hulpmiddelen, de diensten) in overeenstemming met de hieronder gespecificeerde veranderingen te zijn.

## Hoe kan ik bepalen welke algoritmen, verbindingstypes, en protocollen momenteel door mijn organisatie worden gebruikt?

De FTP-/SFTP-software die u gebruikt, moet aangeven welke specifieke instellingen worden gebruikt in de verbindingen die u hebt geconfigureerd voor het uitwisselen van gegevens met Adobe Analytics. Deze software moet ook documentatie over de verschillende beschikbare opties voor verbindingen bevatten. De opties die na deze update worden ondersteund, worden in de branche op ruime schaal ondersteund en geaccepteerd.

De verbindingsopties die worden verwijderd, worden over het algemeen als verouderd beschouwd en worden niet gebruikt in de huidige software. Als u de FTP-/SFTP-software de laatste drie jaar hebt bijgewerkt, hebt u waarschijnlijk al een compatibele verbinding.

## Welke Adobe Analytics-functies gebruiken SFTP voor gegevensinvoer?

De volgende functies bieden een optie voor het uploaden van gegevens naar Adobe Analytics met behulp van SFTP.

* [Classificaties](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-saint.html)

* [Klantkenmerken](https://experienceleague.adobe.com/docs/core-services/interface/services/customer-attributes/attributes.html?lang=en)

* [Gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datafeeds.html)

* [Databronnen](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-datasources.html)

* [Data Warehouse levert rapporten](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-dw-reports.html)

* Bovendien, sommige douaneimplementaties die door worden gecreeerd [Engineering Services](https://experienceleague.adobe.com/docs/analytics/export/ftp-and-sftp/set-up-ftp-accounts/ftp-eng-services.html) kan SFTP gebruiken om gegevens uit te wisselen met Adobe.

## Welke specifieke wijzigingen worden in deze update opgenomen?

Hieronder volgt een gedetailleerde lijst met verbindingen en algoritmen die worden verwijderd en die worden ondersteund:

* Mac-algoritmen voor SFTP-protocol:

   * Wij zullen niet langer steun verlenen aan: hmac-md5, hmac-md5-96, hmac-ripemd160, hmacripemd160@openssh.com, hmac-sha1, hmac-sha1-96, hmac-sha1-etm@openssh.com, umac-64-etm@openssh.com, umac-64@openssh.com

   * Wij zullen alleen maar steun geven aan: hmac-sha2-512-etm@openssh.com, hmac-sha2-256-etm@openssh.com, umac-128-etm@openssh.com, hmac-sha2-512, hmacsha2-256, umac-128@openssh.com

* Cphers-algoritme SFTP-protocol:

   * Wij zullen niet langer steun verlenen aan: 3des-cbc, aes128-cbc, aes128-gcm@openssh.com, aes192-cbc, aes256-cbc, aes256-gcm@openssh.com, arcfour, arcfour128, arcfour256, blowfish-cbc, cast128-cbc, rijndael-cbc@lysator.liu.se

   * Wij zullen alleen maar steun geven aan: aes128-ctr, aes192-ctr, aes256-ctr

* Ondersteunde verbindingen voor SFTP-protocol:

   * Het gebruik van SCP- en synchronisatieopdrachten of verbindingen via het SFTP-protocol wordt niet meer ondersteund

   * We ondersteunen alleen pure SFTP-protocolverbindingen

* Ondersteunde FTP-/SFTP-clients/protocollen:

   * FTP: vsftpd versie 3.0.2-25 of hoger

   * SFTP: openssh versie 7.4p1-21 of hoger
