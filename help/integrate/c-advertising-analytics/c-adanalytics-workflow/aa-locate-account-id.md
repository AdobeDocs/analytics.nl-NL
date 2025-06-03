---
description: Instructies voor het zoeken van je account-id's voor Google Ads en Microsoft Advertising.
title: Account-id's zoeken
feature: Advertising Analytics
exl-id: 2faccfd1-df7b-4b0c-a2f3-23138c39a838
source-git-commit: 586459d99674f01a3b18f84f975a3365ddf2fcd9
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Account-id&#39;s zoeken {#locate-your-account-ids}

Leer hoe u uw account-id&#39;s kunt vinden voor Google Ads en Microsoft Advertising.

## Google-advertenties (AdWords) {#google}

>[!IMPORTANT]
>
>Google Ads gebruikt twee typen accounts:
>
>- MCC-account (My Client Center) en
>- Standaardaccount.
>
>Voor deze integratie met Adobe Analytics, **moet u een Standaard login van de Rekening** gebruiken, niet MCC login van de Rekening. De reden hiervoor is dat een MCC-account fungeert als een &#39;paraplu&#39;-account dat toegang heeft tot meerdere Google Ads-accounts met één aanmelding, terwijl de standaardaccount slechts toegang heeft tot één account per aanmelding. Hoewel Google het koppelen van één e-mail naar vijf accounts ondersteunt, biedt Advertising Analytics nog geen ondersteuning voor deze functie. Eén e-mail kan slechts aan één Google Ads-account worden gekoppeld.

Klik op het accountpictogram rechtsboven om het Google Ads-accountnummer (Customer ID) weer te geven.

![ Google Adds Manager Account ](assets/google-account.png)

## Microsoft Advertising (Bing) {#microsoft}

>[!NOTE]
>
>Als uw Microsoft Advertising-account (voorheen bekend als Bing) gebruikmaakt van de Google-importfunctie, moet u de juiste trackingtekenreeks bijwerken. De tekenreeks voor reeksspatiëring wordt niet automatisch bijgewerkt van de Google-versie naar de juiste Microsoft Advertising-tekenreeks en kan resulteren in niet-opgegeven gegevens. Zie [ wat wordt ingevoerd uit de Advertentie van Google ](https://help.ads.microsoft.com/apex/index/3/en/50851/) in de hulp van Advertising van Microsoft voor meer informatie.

**[!UICONTROL Account ID]** en **[!UICONTROL Manager account ID]** zijn beide vereist.

- De **[!UICONTROL Account ID]** bevindt zich onder **[!UICONTROL Settings]** > **[!UICONTROL Account settings]** > **[!UICONTROL Account ID]** . Zorg ervoor dat u [!UICONTROL Account ID] en NIET [!UICONTROL Account number] gebruikt.
- De **[!UICONTROL Manager account ID]** bevindt zich onder **[!UICONTROL Settings]** > **[!UICONTROL Manager account settings]** > **[!UICONTROL Manager account ID]** . Zorg ervoor dat u [!UICONTROL Manager account ID] en NIET [!UICONTROL Manager account number] gebruikt.

![ de navigatie van Advertising van Microsoft ](assets/bing-id.png)

>[!CONTEXTUALHELP]
>id="adanalytics_ma_account_id"
>title="Account-id"
>abstract="De account-id is een numerieke waarde in de Microsoft Advertising-interface. U kunt dit vinden door te navigeren naar Instellingen > Accountinstellingen > Account-id."

>[!CONTEXTUALHELP]
>id="adanalytics_ma_manager_account_id"
>title="Account-ID beheer"
>abstract="De &#39;Manager account-id&#39; is een numerieke waarde in de Microsoft Advertising-interface. U kunt het vinden door te navigeren aan Montages > de montages van de Rekening van de Manager > identiteitskaart van de Rekening van de Manager."
