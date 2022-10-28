---
description: Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.
keywords: ftp;sftp
title: Verstuur de verzoeken van het Data Warehouse naar servers SFTP
feature: FTP Export
exl-id: 45694647-69ec-45e3-b614-4a936909a338
source-git-commit: 25eccb2b9fe3827e62b0ae98d9bebf7a97b239f5
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 3%

---

# Verstuur de verzoeken van het Data Warehouse naar servers SFTP

Adobe ondersteunt het exporteren van Data Warehouse-aanvragen naar SFTP-servers.

Controleer of de volgende taken zijn voltooid:

Adobe steunt de uitvoer van de verzoeken van de Data Warehouse naar servers SFTP, op voorwaarde dat het volgende wordt voldaan aan:

* `sftp://` protocol wordt gespecificeerd op het gastheergebied (bijvoorbeeld `sftp://ftp.example.com`) en ALLEEN poort 22 wordt gebruikt wanneer een Data Warehouse-rapport wordt aangevraagd. U kunt ook de opdracht `sftp+norename://` zoals hieronder beschreven.
* Adobe `authorized_keys` bestand bevindt zich in het `.ssh` binnen de hoofdmap van de gebruiker waarmee u zich aanmeldt
* De bestemming is niet aan `ftp.omniture.com`. SFTP-protocol tussen interne Adobe-servers wordt niet ondersteund.
* De bestemming steunt één-factor (PKI) authentificatie. Als er een tweeledige uitdaging is, zal de indiening van het verslag mislukken. Zorg ervoor dat uw server niet wordt gevormd om dubbel-factor authentificatie te proberen. Adobe Analytics vereist dat alleen de sleutel en niets anders wordt gebruikt om u aan te melden.
* Adobe steunt encryptie SSHv2, en valt terug naar SSHv1 (de sleutel van RSA slechts).

Met succes een verzoek van de Data Warehouse via SFTP verzenden:

1. Verkrijg `authorized_keys` door een van de ondersteunde gebruikers van uw organisatie te laten contact opnemen met de klantenservice.
1. Nadat dit bestand is opgehaald, meldt u zich aan bij de FTP-site onder dezelfde referenties als die voor de aanvraag van de Data Warehouse worden gebruikt.
1. Navigeer in de hoofdmap naar de map met de naam `.ssh` (als er geen bestaat, maakt u er een) en plaatst u de `authorized_keys` bestand daar.

1. Ga naar de manager van de het verzoekvraag van de Data Warehouse. Configureer het verzoek naar wens en klik vervolgens op **[!UICONTROL Advanced Delivery Options]**.

1. Klik in het pop-upvenster op **[!UICONTROL FTP]** geeft u vervolgens de FTP-site op (inclusief de `sftp://` protocol, zoals `sftp://ftp.omniture.com`) via poort 22.

   Met inbegrip van de `sftp://` protocol is alleen toegestaan bij gebruik van SFTP. Reguliere FTP-aanvragen moeten het protocolvoorvoegsel weglaten (zoals: `ftp.omniture.com` in plaats van `ftp://ftp.omniture.com`).

1. Voer de naam in van de map die u wilt plaatsen in het veld Map. Een map is vereist.
1. Voer dezelfde gebruikersnaam en hetzelfde wachtwoord in als in Stap 2.
1. Klik op **[!UICONTROL Send]**.

Met de opdracht Sftp-PUT wordt een tijdelijk bestand met de extensie .part in de opgegeven map geplaatst. Wanneer het uploaden is voltooid, wordt de naam van de bestandsextensie gewijzigd in de naam van de uiteindelijke extensie, waarna deze klaar is voor gebruik.

Alternatief, `sftp+norename://` kan worden opgegeven in plaats van `sftp://` om het bestand zonder tijdelijke `.part` bestandsnaam tijdens uploaden. Deze aanpak is geschikt wanneer de SFTP-server de bestandsnaam automatisch wijzigt tijdens het uploaden en er geen kans is dat het bestand wordt verwerkt voordat het uploaden is voltooid.
