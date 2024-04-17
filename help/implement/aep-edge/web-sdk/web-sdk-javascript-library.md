---
title: Gegevens naar Adobe Analytics verzenden met de Web SDK JavaScript-bibliotheek
description: Begin met een schone implementatie van SDK van het Web om gegevens naar Adobe Analytics te verzenden gebruikend de bibliotheek JavaScript.
hide: true
hidefromtoc: true
source-git-commit: d4c9bddf18311e13d025ed9d62c0636a33eb7b85
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Gegevens naar Adobe Analytics verzenden met de Web SDK JavaScript-bibliotheek

Dit implementatiepad omvat een nieuwe Web SDK-installatie met behulp van de Web SDK JavaScript-bibliotheek. Andere implementatiepaden worden op afzonderlijke pagina&#39;s behandeld:

* [Web SDK-tagextensie](web-sdk-tag-extension.md): Een nieuwe installatie van SDK van het Web die de de markeringsuitbreiding van SDK van het Web gebruikt. Vergelijkbaar met de JavaScript-bibliotheekaanpak van de Web SDK (deze pagina), behalve dat u de implementatie beheert met tags in de gegevensverzameling van Adobe Experience Platform. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.
* [De uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md): Kies een vloeiende en methodische aanpak om van de Adobe Analytics-tagextensie over te schakelen op de Web SDK-tagextensie. Deze benadering onderdrukt de behoefte om XDM te gebruiken tot uw organisatie klaar is om de diensten van Adobe Experience Platform, zoals Customer Journey Analytics te gebruiken. Gebruik de `data` object in plaats van het `xdm` -object om gegevens naar de Adobe te verzenden.
* [AppMeasurement naar Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md): Een vloeiende en methodische aanpak voor het migreren naar de SDK van het Web, behalve dat er geen tags worden gebruikt. In plaats daarvan kunt u de Adobe Analytics-bibliotheek voor gegevensverzameling (`AppMeasurement.js`) en deze vervangen door de Web SDK JavaScript-bibliotheek (`alloy.js`).

## Voordelen en nadelen van dit implementatiepad

Het gebruik van de Web SDK JavaScript bibliotheek om gegevens naar Adobe Analytics te verzenden heeft zowel voor- als nadelen. Let zorgvuldig op elke optie om te bepalen welke benadering het beste is voor uw organisatie.

| Voordelen | Nadelen |
| --- | --- |
| <ul><li>**Directe benadering**: Dit implementatiepad is eenvoudiger dan benaderingen waarmee bestaande Adobe Analytics-implementaties worden verplaatst. Als u geen huidige implementatie van Adobe Analytics om zich over ongerust te maken hebt, bevolk de toepasselijke gebieden van SDK van het Web XDM.</li><li>**Vooraf gedefinieerd schema**: Als uw organisatie geen behoefte aan uw eigen schema heeft, kunt u eenvoudig het schema gebruiken dat aan Adobe Analytics wordt gericht. Dit concept is zelfs van toepassing als u naar Customer Journey Analytics gaat. Het concept &#39;props&#39; en &#39;eVars&#39; zijn niet van toepassing op Customer Journey Analytics, maar u kunt &#39;props&#39; en &#39;eVars&#39; blijven gebruiken als eenvoudige aangepaste afmetingen.</li></ul> | <ul><li>**Implementatiewijzigingen vereisen ingrijpen van de ontwikkelaar**: Als u veranderingen in uw implementatie van SDK van het Web wilt aanbrengen, moet u met uw ontwikkelingsteam werken om de code op uw plaats uit te geven. De methode die gebruikmaakt van de [Web SDK-tagextensie](web-sdk-tag-extension.md) voorkomt dit nadeel.</li><li>**Vergrendeld in een specifiek schema**: Wanneer uw organisatie naar Customer Journey Analytics gaat, moet u het Adobe Analytics-schema blijven gebruiken of naar het schema van uw eigen organisatie migreren (wat een aparte gegevensset zou zijn). Als uw organisatie zowel het Adobe Analytics-schema als de migratie naar een aparte gegevensset bij de overgang naar de Customer Journey Analytics wil vermijden, raadt Adobe een van de volgende twee methoden aan:</li><ul><li>Gebruik de `data` object: Het `data` kunt u gegevens naar Adobe Analytics verzenden zonder aan een XDM-schema te voldoen. Zodra het schema van uw organisatie wordt gecreeerd, kunt u gegevenstoewijzing aan kaart gebruiken `data` objectvelden naar XDM. Beide [De uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md) en [AppMeasurement naar Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md) gebruiken `data` object.</li><li>Adobe Analytics volledig overslaan: als u de SDK van het Web implementeert, kunt u die gegevens naar een dataset in Adobe Experience Platform verzenden voor gebruik in Customer Journey Analytics. U kunt elk schema gebruiken dat u bevalt. Adobe Analytics is helemaal niet betrokken bij deze workflow en vereist daarom niet de Adobe Analytics ExperienceEvent-veldgroep. Deze methode leidt tot het minste bedrag aan technische schulden, maar laat Adobe Analytics ook volledig buiten beeld.</li></ul></ul> |
