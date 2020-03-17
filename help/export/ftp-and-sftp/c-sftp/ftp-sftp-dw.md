---
description: Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.
keywords: ftp;sftp
title: Verstuur de verzoeken van het Pakhuis van Gegevens naar servers SFTP
uuid: 393634a1-0643-4d63-bb6e-fb80f1ba76c1
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Verstuur de verzoeken van het Pakhuis van Gegevens naar servers SFTP

Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.

Controleer of de volgende taken zijn voltooid:

Adobe ondersteunt de export van Data Warehouse-aanvragen naar SFTP-servers, op voorwaarde dat aan het volgende wordt voldaan:

* [!DNL sftp://] Het protocol wordt gespecificeerd op het gastheergebied (bijvoorbeeld, [!DNL sftp://ftp.example.com]) en SLECHTS haven 22 wordt gebruikt wanneer het verzoeken van een rapport van het Pakhuis van Gegevens.

   U kunt de [!DNL sftp+norename://] optie ook gebruiken, zoals hieronder beschreven.

* Het Adobe- [!DNL authorized_keys] bestand staat in de [!DNL .ssh] map in de hoofdmap van de gebruiker waarmee u zich aanmeldt

* De bestemming is niet aan [!DNL ftp.omniture.com]. SFTP-protocol tussen de interne servers van Adobe wordt niet ondersteund.
* De bestemming steunt één-factor (PKI) authentificatie. Als er een tweeledige uitdaging is, zal de indiening van het verslag mislukken. Zorg ervoor dat uw server niet is geconfigureerd voor verificatie met twee factoren. Voor Adobe Analytics moet alleen de sleutel en niets anders worden gebruikt om u aan te melden.
* Adobe ondersteunt SSHv2-codering en wordt teruggezet naar SSHv1 (alleen RSA-sleutel).

Een [!DNL Data Warehouse] aanvraag verzenden via SFTP:

1. Haal het [!DNL authorized_keys] bestand op door een van de ondersteunde gebruikers van uw organisatie contact op te nemen met de klantenservice.
1. Nadat dit bestand is opgehaald, meldt u zich aan bij de FTP-site onder dezelfde referenties als die voor de [!DNL Data Warehouse] aanvraag worden gebruikt.
1. Navigeer in de hoofdmap naar de map met de naam [!DNL .ssh] (als deze niet bestaat, maak er een) en plaats het [!DNL authorized_keys] bestand daar.

1. Ga naar de [!DNL Data Warehouse] aanvraagmanager. Configureer de aanvraag naar wens en klik op **[!UICONTROL Advanced Delivery Options]**.

1. Klik in het pop-upvenster **[!UICONTROL FTP]** en geef vervolgens de FTP-site (inclusief het [!DNL sftp://] protocol, zoals [!DNL sftp://ftp.omniture.com]) via poort 22 op.

   Het opnemen van het [!DNL sftp://] protocol is alleen toegestaan bij gebruik van SFTP. Reguliere FTP-aanvragen moeten het protocolvoorvoegsel weglaten (bijvoorbeeld, [!DNL ftp.omniture.com] in plaats van [!DNL ftp://ftp.omniture.com]).

1. Voer de naam in van de map die u wilt plaatsen in het veld Map. Een map is vereist.
1. Voer dezelfde gebruikersnaam en hetzelfde wachtwoord in als in Stap 2.
1. Klik op **[!UICONTROL Send]**.

Met de opdracht Sftp PUT wordt een tijdelijk bestand met de extensie .part in de opgegeven map geplaatst. Wanneer het uploaden is voltooid, wordt de naam van de bestandsextensie gewijzigd in de naam van de uiteindelijke extensie, waarna deze klaar is voor gebruik.

U [!DNL sftp+norename://] kunt ook opgeven dat u het bestand zonder tijdelijke [!DNL sftp://] [!DNL .part] bestandsnaam tijdens het uploaden niet rechtstreeks met de uiteindelijke naam wilt uploaden, maar dat u het bestand ook zonder de definitieve naam wilt uploaden. Deze aanpak is geschikt wanneer de SFTP-server de bestandsnaam automatisch wijzigt tijdens het uploaden en er geen kans is dat het bestand wordt verwerkt voordat het uploaden is voltooid.
