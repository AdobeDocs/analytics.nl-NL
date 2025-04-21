---
description: Algemene problemen bij het gebruik van Report Builder met Power BI.
title: Problemen met Power BI-integratie oplossen
feature: Report Builder
role: User, Admin
exl-id: adb13a0e-99fb-48f5-add2-204d155e467f
source-git-commit: 73c0210ac931f3e7f823e033a3bffdc22e159ddb
workflow-type: tm+mt
source-wordcount: '311'
ht-degree: 0%

---

# Problemen met Power BI-integratie oplossen

{{legacy-arb}}

Onderzoek en los gemeenschappelijke kwesties op wanneer het gebruiken van Report Builder met Power BI.

## Publiceren naar Power BI is mislukt

Geplande werkboeken waarvoor publicatie door Power BI vereist is, zijn afhankelijk van Power BI-services om in gebruik te zijn. Twee belangrijke redenen voor het niet publiceren zijn:

* Power BI-services zijn mogelijk niet beschikbaar.
* De gebruiker die het werkboek opende heeft niet meer geldige de rekeningsgeloofsbrieven van Microsoft.

Elke geplande Report Builder-taak krijgt drie pogingen per geplande uitvoering:

* Na de eerste mislukte poging krijgt u het volgende bericht: &quot;&quot;We konden dit geplande werkboek niet publiceren naar Microsoft Power BI. We proberen het binnenkort opnieuw.&quot;
* Na de tweede mislukte poging krijg je geen bericht meer.
* Na de derde mislukte poging krijgt u het volgende bericht: &quot;We konden dit werkboek niet publiceren naar Power BI.&quot;

## Gebroken visualisaties in Power BI

Hieronder vindt u een overzicht van de belangrijkste redenen waarom u een verbroken weergave kunt krijgen nadat u Report Builder-verzoeken naar Power BI hebt gepubliceerd:

* U hebt een aanvraag bewerkt in Report Builder, zoals metriek of afmetingen wijzigen en vervolgens opnieuw gepubliceerd naar Power BI. Door aanvragen te bewerken kunnen uw visualisaties worden verbroken.
* U hebt een aanvraag verwijderd die in een visualisatie is gebruikt.

>[!IMPORTANT]
>
>Report Builder vereist dat een beheerder toegang tot uw organisatiebronnen toestaat. Als u toegang nodig hebt, vraagt u een beheerder om u toestemming te verlenen.
> Een Admin van Microsoft kan de *Gebruikers herzien kan toepassing* registreren die onder wordt gevonden: **[!UICONTROL Microsoft Azure]** > **[!UICONTROL Azure Active Directory]** > **[!UICONTROL User Settings allows options]**. Als deze optie aan **Nr** wordt geplaatst, dan kan admin deze soorten toepassingen registreren.

De gebruikers kunnen Toegang verlenen door in hun [ Microsoft Power BI rekening ](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=logint&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US) te registreren.

Admins kunnen toegang voor elk verlenen door in hun [ rekening van Microsoft Power BI van de Beheerder te registreren ](https://login.microsoftonline.com/common/oauth2/authorize?response_type=code&amp;prompt=admin_consent&amp;client_id=8d84f6d8-29a4-4484-a670-589b32400278&amp;redirect_uri=https%3a%2f%2fmy.omniture.com%2fsc15%2farb%2flogin.html&amp;resource=https%3a%2f%2fanalysis.windows.net%2fpowerbi%2fapi&amp;locale=en_US).

## De API-limiet bereiken

Rapportering in Power BI werkt met de API voor analyserapportage, zodat de API-drempelwaarden van toepassing zijn.
