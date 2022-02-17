---
title: Aanmelden bij Adobe Analytics oplossen
description: Stappen die moeten worden uitgevoerd wanneer u zich niet kunt aanmelden bij Adobe Analytics.
feature: Analytics Basics
exl-id: e670a043-c55b-4717-9b60-613ea4d04382
source-git-commit: c8faf29262b9b04fc426f4a26efaa8e51293f0ec
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 2%

---

# Aanmelden bij Adobe Analytics oplossen

Adobe Analytics gebruikt meerdere verificatiemethoden om u aan te melden:

* Adobe ID door de Experience Cloud
* Legacy Analytics ID
* Eenmalige aanmelding

**Als u regelmatig toegang hebt tot Analytics en willekeurig begint aanmeldingsproblemen op te lossen, kunt u de meeste problemen verhelpen door de cookies en cache van uw browser te wissen.**

Soms, kunnen de beschikbaarheidskwesties de capaciteit beïnvloeden om aan login. Controleren [status.adobe.com](https://status.adobe.com) voor openstaande incidenten. Anders, gebruik de aangewezen sectie afhankelijk van de authentificatiemethode van uw organisatie.

## Adobe ID

Los problemen met het aanmelden bij Adobe Analytics op met de Experience Cloud.

1. Navigeren naar [experience.adobe.com](https://experience.adobe.com). Als u geen toegang hebt tot deze site, is het mogelijk dat uw organisatie dit domein niet toestaat via uw firewall. Werk met het IT-team van uw organisatie om dit mogelijk te maken. Zie [In de Adobe Experience Cloud gebruikte IP&#39;s en domeinen](https://helpx.adobe.com/nl/analytics/kb/adobe-ip-addresses.html) voor nuttige informatie aan uw team van IT.

2. Verifiëren met Adobe ID: Klikken **[!UICONTROL Sign In with an Adobe ID]**. Als u zich niet kunt aanmelden, controleert u nogmaals of uw e-mailadres correct is getypt. Anders klikt u op **[!UICONTROL Reset password]** en volgt u de aanwijzingen om uw Adobe ID-wachtwoord opnieuw in te stellen.

3. Access Analytics after authenticating: Klik op het pictogram met het 9-raster rechtsboven in het scherm en klik vervolgens op Analytics. Als u deze optie niet hebt of deze grijs is, werkt u samen met een productbeheerder binnen uw organisatie om ervoor te zorgen dat u de juiste machtigingen hebt om toegang te krijgen tot Analytics.

## Legacy Analytics ID

Een gebruiker in uw organisatie kan de volgende fout ontvangen wanneer hij of zij zich aanmeldt:

*Dit account is uit veiligheidsoverwegingen vergrendeld vanwege te veel mislukte aanmeldingspogingen.*

Als het wissen van de cookies/cache van de browser het probleem niet verhelpt, werkt u samen met een analysebeheerder in uw organisatie om het wachtwoord van de gebruiker opnieuw in te stellen.

>[!IMPORTANT]
>
>De volgende stappen voor het opnieuw instellen van het wachtwoord van een gebruiker zijn alleen van toepassing op verouderde Analytics ID&#39;s, niet op Adobe ID. Als uw organisatie gebruikmaakt van Adobe ID, kunt u gebruikersaccounts beheren op [adminconsole.adobe.com](https://adminconsole.adobe.com).

1. Meld u aan bij Adobe Analytics met een account met beheerdersrechten.
2. Ga naar **[!UICONTROL Admin]** > **[!UICONTROL All admin]** > **[!UICONTROL User management]**.
3. Klik op de knop **[!UICONTROL Users]** en klik vervolgens op **[!UICONTROL Edit]** naast de gewenste gebruiker.
4. Wijzig het wachtwoord in een willekeurige waarde en schakel het selectievakje in **[!UICONTROL Require user to change password on next login]**.
5. Stel de gebruiker op de hoogte van het nieuwe wachtwoord.

## Eenmalige aanmelding

Neem contact op met een beheerder in uw organisatie om problemen met eenmalige aanmelding op te lossen.

## Verlopen aanmeldingen

Een gebruiker in uw organisatie kan de volgende fout ontvangen wanneer hij of zij zich aanmeldt:

*Fout: Deze aanmelding is verlopen.*

Deze fout werkt zoals bedoeld. Adobe Analytics biedt beheerders de mogelijkheid om een datumbereik in te stellen dat geldig is voor een gebruikersaccount. Als de huidige datum buiten de geldige datumwaaier voor de rekening verblijft, kunnen zij niet login. Werk met een analysebeheerder in uw organisatie om het geldige datumbereik van de aanmelding uit te breiden. De klantenservice van Adobe is niet bevoegd om geldige aanmeldingsdatumbereiken voor gebruikersaccounts te wijzigen.

## Andere aanmeldingsproblemen

Als geen van de bovenstaande stappen werkt, bepaalt u de breedte van het aanmeldingsprobleem:

* Komt het probleem voor wanneer het gebruiken van verschillende browser, of is het over alle browsers?
* Komt de kwestie op een verschillende machine op het netwerk voor, of is het over veelvoudige machines?
* Meld u aan via een ander netwerk, zoals een mobiele gegevensverbinding, bibliotheek of thuisnetwerk. Is de kwestie aanwezig over netwerken?

Als de kwestie binnen uw netwerk geïsoleerd is, werk met het team van IT van uw organisatie om het op te lossen. Neem contact op met de klantenservice van Adobe als dit niet beperkt is tot één netwerk.
