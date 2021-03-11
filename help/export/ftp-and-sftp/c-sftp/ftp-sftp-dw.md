---
description: Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.
keywords: ftp;sftp
title: Verstuur de verzoeken van het Data Warehouse naar servers SFTP
uuid: 393634a1-0643-4d63-bb6e-fb80f1ba76c1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 3%

---


# Verstuur de verzoeken van het Data Warehouse naar servers SFTP

Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.

Controleer of de volgende taken zijn voltooid:

Adobe steunt de uitvoer van de verzoeken van de Data Warehouse naar servers SFTP, op voorwaarde dat het volgende wordt voldaan aan:

* [!DNL sftp://] protocol wordt gespecificeerd op het gastheergebied (bijvoorbeeld,  [!DNL sftp://ftp.example.com]) en SLECHTS haven 22 wordt gebruikt wanneer het verzoeken van een rapport van de Data Warehouse.

   U kunt ook de optie [!DNL sftp+norename://] gebruiken, zoals hieronder beschreven.

* Het bestand [!DNL authorized_keys] bevindt zich in de map [!DNL .ssh] in de hoofdmap van de gebruiker waarmee u zich aanmeldt

* De bestemming is niet aan [!DNL ftp.omniture.com]. SFTP-protocol tussen interne Adobe-servers wordt niet ondersteund.
* De bestemming steunt één-factor (PKI) authentificatie. Als er een tweeledige uitdaging is, zal de indiening van het verslag mislukken. Zorg ervoor dat uw server niet is geconfigureerd voor verificatie met twee factoren. Adobe Analytics vereist dat alleen de sleutel en niets anders wordt gebruikt om u aan te melden.
* Adobe steunt encryptie SSHv2, en valt terug naar SSHv1 (de sleutel van RSA slechts).

Om een [!DNL Data Warehouse] verzoek via SFTP met succes te verzenden:

1. Verkrijg het [!DNL authorized_keys] dossier door één van de gesteunde gebruikers van uw organisatie te laten de Zorg van de Klant contacteren.
1. Nadat dit bestand is verkregen, meldt u zich aan bij de FTP-site onder dezelfde referenties als die voor het [!DNL Data Warehouse]-verzoek worden gebruikt.
1. Navigeer in de hoofdmap naar de map [!DNL .ssh] (als deze niet bestaat, maakt u er een) en plaats het bestand [!DNL authorized_keys] daar.

1. Ga naar [!DNL Data Warehouse] aanvraagmanager. Vorm het verzoek zoals gewenst, dan klik **[!UICONTROL Advanced Delivery Options]**.

1. Klik in het pop-upvenster op **[!UICONTROL FTP]** en geef vervolgens de ftp-site (inclusief het [!DNL sftp://]-protocol, zoals [!DNL sftp://ftp.omniture.com]) via poort 22 op.

   Het opnemen van het [!DNL sftp://]-protocol is alleen toegestaan bij gebruik van SFTP. Reguliere FTP-aanvragen moeten het protocolvoorvoegsel weglaten (zoals [!DNL ftp.omniture.com] in plaats van [!DNL ftp://ftp.omniture.com]).

1. Voer de naam in van de map die u wilt plaatsen in het veld Map. Een map is vereist.
1. Voer dezelfde gebruikersnaam en hetzelfde wachtwoord in als in Stap 2.
1. Klik op **[!UICONTROL Send]**.

Met de opdracht Sftp-PUT wordt een tijdelijk bestand met de extensie .part in de opgegeven map geplaatst. Wanneer het uploaden is voltooid, wordt de naam van de bestandsextensie gewijzigd in de naam van de uiteindelijke extensie, waarna deze klaar is voor gebruik.

U kunt ook [!DNL sftp+norename://] opgeven in plaats van [!DNL sftp://] om het bestand direct met de definitieve naam te uploaden, zonder een tijdelijke [!DNL .part]-bestandsnaam tijdens het uploaden. Deze aanpak is geschikt wanneer de SFTP-server de bestandsnaam automatisch wijzigt tijdens het uploaden en er geen kans is dat het bestand wordt verwerkt voordat het uploaden is voltooid.
