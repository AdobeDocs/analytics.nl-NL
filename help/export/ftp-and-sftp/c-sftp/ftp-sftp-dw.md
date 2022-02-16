---
description: Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.
keywords: ftp;sftp
title: Verstuur de verzoeken van het Data Warehouse naar servers SFTP
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
source-git-commit: 4daa5c8bdbcb483f23a3b8f75dde9eeb48516db8
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 3%

---

# Verstuur de verzoeken van het Data Warehouse naar servers SFTP

Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.

Controleer of de volgende taken zijn voltooid:

Adobe steunt de uitvoer van de verzoeken van de Data Warehouse naar servers SFTP, op voorwaarde dat het volgende wordt voldaan aan:

* [!DNL sftp://] protocol wordt gespecificeerd op het gastheergebied (bijvoorbeeld [!DNL sftp://ftp.example.com]) en ALLEEN poort 22 wordt gebruikt wanneer een Data Warehouse-rapport wordt aangevraagd.

   U kunt ook de opdracht [!DNL sftp+norename://] zoals hieronder beschreven.

* Adobe [!DNL authorized_keys] bestand bevindt zich in het [!DNL .ssh] binnen de hoofdmap van de gebruiker waarmee u zich aanmeldt

* De bestemming is niet aan [!DNL ftp.omniture.com]. SFTP-protocol tussen interne Adobe-servers wordt niet ondersteund.
* De bestemming steunt één-factor (PKI) authentificatie. Als er een tweeledige uitdaging is, zal de indiening van het verslag mislukken. Zorg ervoor dat uw server niet is geconfigureerd voor verificatie met twee factoren. Adobe Analytics vereist dat alleen de sleutel en niets anders wordt gebruikt om u aan te melden.
* Adobe steunt encryptie SSHv2, en valt terug naar SSHv1 (de sleutel van RSA slechts).

Als u een [!DNL Data Warehouse] verzoek via SFTP:

1. Verkrijg [!DNL authorized_keys] door een van de ondersteunde gebruikers van uw organisatie te laten contact opnemen met de klantenservice.
1. Nadat dit bestand is verkregen, meldt u zich aan bij de FTP-site onder dezelfde referenties als die voor de [!DNL Data Warehouse] verzoek.
1. Navigeer in de hoofdmap naar de map met de naam [!DNL .ssh] (als er geen bestaat, maakt u er een) en plaatst u de [!DNL authorized_keys] bestand daar.

1. Ga naar de [!DNL Data Warehouse] aanvraagmanager. Configureer het verzoek naar wens en klik vervolgens op **[!UICONTROL Advanced Delivery Options]**.

1. Klik in het pop-upvenster op **[!UICONTROL FTP]** geeft u vervolgens de FTP-site op (inclusief de [!DNL sftp://] protocol, zoals [!DNL sftp://ftp.omniture.com]) via poort 22.

   Met inbegrip van de [!DNL sftp://] protocol is alleen toegestaan bij gebruik van SFTP. Reguliere FTP-aanvragen moeten het protocolvoorvoegsel weglaten (zoals: [!DNL ftp.omniture.com] in plaats van [!DNL ftp://ftp.omniture.com]).

1. Voer de naam in van de map die u wilt plaatsen in het veld Map. Een map is vereist.
1. Voer dezelfde gebruikersnaam en hetzelfde wachtwoord in als in Stap 2.
1. Klik op **[!UICONTROL Send]**.

Met de opdracht Sftp-PUT wordt een tijdelijk bestand met de extensie .part in de opgegeven map geplaatst. Wanneer het uploaden is voltooid, wordt de naam van de bestandsextensie gewijzigd in de naam van de uiteindelijke extensie, waarna deze klaar is voor gebruik.

Alternatief, [!DNL sftp+norename://] kan worden opgegeven in plaats van [!DNL sftp://] om het bestand zonder tijdelijke [!DNL .part] bestandsnaam tijdens uploaden. Deze aanpak is geschikt wanneer de SFTP-server de bestandsnaam automatisch wijzigt tijdens het uploaden en er geen kans is dat het bestand wordt verwerkt voordat het uploaden is voltooid.
