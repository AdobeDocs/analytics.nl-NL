---
description: Vaak voorkomende problemen bij het gebruik van Report Builder met Power BI.
title: Problemen met Power BI-integratie oplossen
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: a30564e9d8969457aaa8709c3aa3c17ba6d0a2d3
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 2%

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

Rapportage in Power BI werkt met de API voor analyserapportage, zodat de API-drempelwaarden van toepassing zijn. Zie voor meer informatie [Wat is de tariefgrens voor API vraag?](https://developer.adobe.com/analytics-apis/docs/2.0/guides/faq/#what-is-the-rate-limit-for-api-calls).
