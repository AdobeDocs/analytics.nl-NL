---
description: Vaak voorkomende problemen bij het gebruik van Report Builder met Power BI.
title: Problemen met Power BI-integratie oplossen
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: b98fbf52ab9fefef9c19e82f440ca9f5a81f933f
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Problemen met Power BI-integratie oplossen

Onderzoek en los gemeenschappelijke kwesties op wanneer het gebruiken van Report Builder met Power BI.

## Publiceren naar Power BI is mislukt

De geplande werkboeken die Power BI het publiceren vereisen zijn afhankelijk van de diensten van Power BI om in werking te zijn. Twee belangrijke redenen voor het niet publiceren zijn:

* De diensten van de Power BI kunnen neer zijn.
* De gebruiker die het werkboek opende heeft niet meer geldige de rekeningsgeloofsbrieven van Microsoft.

Elke geplande Report Builder taak krijgt drie pogingen per geplande looppas:

* Na de eerste mislukte poging ontvangt u het volgende bericht: &quot;&quot;We konden dit geplande werkboek niet publiceren naar Microsoft Power BI. We proberen het binnenkort opnieuw.&quot;
* Na de tweede mislukte poging krijg je geen bericht meer.
* Na de derde mislukte poging ontvangt u het volgende bericht: &quot;We konden dit werkboek niet naar Power BI publiceren.&quot;

## Gebroken visualisaties in Power BI

Hieronder vindt u een overzicht van de belangrijkste redenen waarom u onderbroken visualisaties kunt krijgen nadat u Report Builder-verzoeken naar Power BI hebt gepubliceerd:

* U hebt een aanvraag bewerkt in Report Builder, zoals metriek of afmetingen wijzigen en vervolgens opnieuw gepubliceerd in Power BI. Door aanvragen te bewerken kunnen uw visualisaties worden verbroken.
* U hebt een aanvraag verwijderd die in een visualisatie is gebruikt.

## Report Builder moet gemachtigd zijn om toegang te krijgen tot uw organisatiebronnen. Deze toegang kan slechts door een beheerder worden verleend. Vraag een beheerder om u toestemming te verlenen.

Laat een Microsoft-beheerder de instelling Gebruikers kunnen de toepassing registreren bekijken onder: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL User Settings allows options]**. Als deze optie is ingesteld op Nee, kan die beheerder deze typen toepassingen registreren.

Gebruikers kunnen toegang verlenen door het volgende te gebruiken: [link](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

Beheerders die toegang voor elke instantie hebben verkregen, gebruiken het volgende [link](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

## De API-limiet bereiken

Rapportage in Power BI werkt met de API voor analyserapportage, zodat de API-drempelwaarden van toepassing zijn. Voor Analytics 2.0 APIs, wordt de throttle grens geplaatst bij 120 vraag per minuut, per gebruiker, ongeacht rapportreeks of bedrijf. Wanneer de throttle grens wordt gepasseerd, keert de server een HTTP 429 status aan de gebruiker met deze berichtinhoud terug:

```
too many requests
{"error_code":"429050","message":"Too many requests"}
```

Adobe raadt u aan *naleven* de volgende richtsnoeren:

* Maak veelvoudige, kleinere verzoeken in plaats van een grote, enige aanvraag.
* Vraag gegevens eenmaal aan en cachegeheugen deze in.
* U mag niet sneller dan een interval van 30 minuten opiniepeilen voor nieuwe gegevens.
* Trek historische gegevens en verhoogt het regelmatig in plaats van om de volledige gegevensreeks te verzoeken.

Adobe raadt u aan *vermijden* het volgende:

* zoveel mogelijk gegevens in één aanvraag aanvragen
* Vraag elke dag één jaar aan gegevens bij daggranulariteit om een rolend venster van 12 maanden. Adobe raadt u aan in plaats daarvan de gegevens van de nieuwe dag op te vragen en deze samen te voegen met de bestaande gegevens van vorige dagen.
* Een webpagina met een widget voor siteprestaties besturen door elke keer dat de webpagina wordt geladen een API-verzoek in te dienen
* Migreren vanaf 1,4
