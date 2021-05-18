---
title: Einde van levensduur voor [!UICONTROL Enforce IP login restrictions]
description: Meer informatie over de timing en implicaties voor [!UICONTROL Enforce IP login restrictions] aan het einde van de levensduur
exl-id: 67d822ee-005b-46cf-80b4-a5aa4412d746
source-git-commit: d198e8ef0ec8415a4a555d3c385823baad6104fe
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# Einde van levensduur voor [!UICONTROL Enforce IP login restrictions]

Met de functie **[Inlogbeperkingen voor IP afdwingen](/help/admin/company/security-manager.md)** in Adobe Analytics kunt u specifieke IP-adressen (die veilig worden geacht) toevoegen aan een lijst van gewenste personen, zodat u zich met succes kunt aanmelden en toegang hebt tot uw Adobe Analytics-omgeving. In veel gevallen, wordt deze eigenschap gebruikt aan opstelling een collectief IP adres als enig veilig IP adres dat de gebruikers kunnen login van. Daarom om Adobe Analytics te gebruiken, vereist dit gebruikers om bij een collectief bureau of het netwerk via VPN te zijn login.

We zijn van plan om deze functie in januari 2021 te beëindigen.

## Waarom zijn we aan het einde van deze functie?

Deze functie wordt in sommige gevallen onderbroken door de Experience Cloud-aanmeldmigratie en/of de Experience Cloud-aanmelding. Het is bekend dat deze functie wordt onderbroken voor klanten die **[!UICONTROL Customer Attributes]** of **[!UICONTROL Audience Library]** gebruiken.

Bovendien, als u veelvoudige Oplossingen van Experience Cloud bezit, kunt u dit vereiste omzeilen door aan de Experience Cloud met één van de andere oplossingen het programma te openen, aangezien deze eigenschap niet bestaat of niet buiten Analytics zelf wordt gesteund. Gebruikers konden dit ook omzeilen via IP-spoofing.

Tot slot heeft Adobe een functionerende en veel superieure alternatieve oplossing via Single Sign-On en Federated IDs. Met deze functie hebt u meer controle en beveiliging over de aanmeldervaring van uw gebruikers. Zie hieronder voor meer informatie.

## Hoe beïnvloedt het verwijderen van deze functie u?

Voor elke klant die **[!UICONTROL Enforce IP login restrictions]** heeft ingesteld, wordt deze functie verwijderd in januari 2021. Op dat ogenblik, zullen om het even welke IP login beperkingen nog op zijn plaats niet meer worden afgedwongen. Als u login door IP adres nog moet beperken, zou u de geadviseerde oplossing van Single-Sign-On en Federated IDs (meer info en middelen hieronder) moeten herzien en uitvoeren.

Daarnaast wordt de **[!UICONTROL Enforce IP login restrictions]**-instelling verwijderd uit **[!UICONTROL Admin]> [!UICONTROL All admin] > [!UICONTROL Company settings] >[!UICONTROL Security Manager]** in de analysefunctie (zoals hieronder wordt getoond).

![](assets/sec-manager2.png)

## Wat zijn uw andere opties?

Zoals hierboven vermeld, wordt deze functie Analytics opgeheven. Om u tijd te geven om SSO en Federated IDs uit te voeren, hebben wij de datum EOL tot Januari 2021 vertraagd.

Zowel SSO als Federated IDs zijn superieure oplossingen aan de IP eigenschap van de Beperking van de Aanmelding die wij vandaag op zijn plaats hebben en u van meer controle, veiligheid en eigenschappen voorzien. Voor informatie over hoe te opstelling SSO/Federated IDs, hebben wij de volgende hulpdocumentatie beschikbaar. Wij adviseren dat u hen grondig leest en met uw afdeling van IT werkt om hen te krijgen uitgevoerd:

* [Single Sign-On en de Experience Cloud](https://spark.adobe.com/page/JeSB8EPEQIvjD/)
* [Admin Console - documentatie voor identiteitsinstellingen](https://helpx.adobe.com/enterprise/using/set-up-identity.html)
* [Admin Console - Zelfstudie Identiteitsinstellingen (video)](https://helpx.adobe.com/enterprise/how-to/identity-directories-domains.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&amp;ref=helpx.adobe.com)
* [Zelfstudie Federated ID configureren (video)](https://helpx.adobe.com/enterprise/how-to/identity-configure-ids.html?playlist=/ccx/v1/collection/product/enterprise/topics/enterprise-identity/collection.ccx.js&amp;ref=helpx.adobe.com)
* [Single Sign On - veelvoorkomende vragen](https://helpx.adobe.com/enterprise/using/sso-faq.html)
* [Door Adobe ondersteunde identiteitstypen](https://helpx.adobe.com/enterprise/using/identity.html)

Als u uw steun voor IP Login Beperkingen wilt blijven uitdrukken en om het te verzoeken dat het door de Experience Cloud wordt verstrekt, kunt u voor deze eigenschap op onze [pagina van het Forum](https://forums.adobe.com/ideas/11648) stemmen.
