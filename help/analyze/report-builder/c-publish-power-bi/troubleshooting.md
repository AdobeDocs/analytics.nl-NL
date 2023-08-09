---
description: Vaak voorkomende problemen bij het gebruik van Report Builder met Power BI.
title: Problemen met Power BI-integratie oplossen
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: fb39f906d6c08713e4dc8211c917b2942502868e
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 1%

---

# Problemen met Power BI-integratie oplossen

Onderzoek en los gemeenschappelijke kwesties op wanneer het gebruiken van Report Builder met Power BI.

## Publiceren naar Power BI is mislukt

De geplande werkboeken die Power BI het publiceren vereisen zijn afhankelijk van de diensten van Power BI om in werking te zijn. Twee belangrijke redenen voor het niet publiceren zijn:

* De diensten van de Power BI kunnen neer zijn.
* De gebruiker die het werkboek opende heeft niet meer geldige de rekeningsgeloofsbrieven van Microsoft.

Elke geplande Report Builder taak krijgt drie pogingen per geplande looppas:

* Na de eerste mislukte poging krijgt u het volgende bericht: &quot;&quot;We konden dit geplande werkboek niet publiceren naar Microsoft Power BI. We proberen het binnenkort opnieuw.&quot;
* Na de tweede mislukte poging krijg je geen bericht meer.
* Na de derde mislukte poging krijgt u het volgende bericht: &quot;We konden dit werkboek niet naar Power BI publiceren.&quot;

## Gebroken visualisaties in Power BI

Hieronder vindt u een overzicht van de belangrijkste redenen waarom u onderbroken visualisaties kunt krijgen nadat u Report Builder-verzoeken naar Power BI hebt gepubliceerd:

* U hebt een aanvraag bewerkt in Report Builder, zoals metriek of afmetingen wijzigen en vervolgens opnieuw gepubliceerd in Power BI. Door aanvragen te bewerken kunnen uw visualisaties worden verbroken.
* U hebt een aanvraag verwijderd die in een visualisatie is gebruikt.

>[!IMPORTANT]
>
>Report Builder vereist een beheerder om toegang tot uw organisatiemiddelen toe te staan. Als u toegang nodig hebt, vraagt u een beheerder om u toestemming te verlenen.
> Een Microsoft-beheerder kan de *Gebruikers kunnen een toepassing registreren* instelling gevonden onder: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL User Settings allows options]**. Als deze optie is ingesteld op **Nee**, kan de beheerder deze typen toepassingen registreren.

Gebruikers kunnen toegang verlenen door zich aan te melden [Microsoft Power BI account](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

Beheerders kunnen toegang verlenen voor elke gebruiker door zich aan te melden bij hun [Microsoft-Power BI-account van beheerder](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

## De API-limiet bereiken

Rapportage in Power BI werkt met de API voor analyserapportage, zodat de API-drempelwaarden van toepassing zijn. Zie voor meer informatie [Foutcodes voor webservices](https://github.com/AdobeDocs/analytics-1.4-apis/blob/3dda746890743c2098256719d6595109b7748262/docs/getting-started/c_Web_Services_Error_Codes.md).
