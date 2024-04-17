---
title: Gegevens naar Adobe Analytics verzenden met de Web SDK-tagextensie
description: Begin met een schone implementatie van de Gegevensinzameling van Adobe Experience Platform om gegevens naar Adobe Analytics te verzenden gebruikend XDM en de het gebiedsgroep van Adobe Analytics ExperienceEvent.
hide: true
hidefromtoc: true
source-git-commit: d4c9bddf18311e13d025ed9d62c0636a33eb7b85
workflow-type: tm+mt
source-wordcount: '611'
ht-degree: 0%

---

# Gegevens naar Adobe Analytics verzenden met de Web SDK-tagextensie

Dit implementatiepad omvat een nieuwe Web SDK-installatie met tags in Adobe Experience Platform Data Collection. Andere implementatiepaden worden op afzonderlijke pagina&#39;s behandeld:

* [Web SDK JavaScript-bibliotheek](web-sdk-javascript-library.md): Een nieuwe Web SDK-installatie met de Web SDK JavaScript-bibliotheek (`alloy.js`). Gelijkaardig aan de de marktextensiebenadering van SDK van het Web (deze pagina), behalve beheert u de implementatie zelf in plaats van het gebruiken van de markeringen UI. Hiervoor is de Adobe Analytics ExperienceEvent-veldgroep vereist, die typische analytische variabelen bevat die in uw XDM-schema moeten worden opgenomen.
* [De uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md): Kies een vloeiende en methodische aanpak om van de Adobe Analytics-tagextensie over te schakelen op de Web SDK-tagextensie. Deze benadering onderdrukt de behoefte om XDM te gebruiken tot uw organisatie klaar is om de diensten van Adobe Experience Platform, zoals Customer Journey Analytics te gebruiken. Gebruik de `data` object in plaats van het `xdm` -object om gegevens naar de Adobe te verzenden.
* [AppMeasurement naar Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md): Een vloeiende en methodische aanpak voor het migreren naar de SDK van het Web, behalve dat er geen tags worden gebruikt. In plaats daarvan verwijdert u handmatig de Adobe Analytics-bibliotheek voor gegevensverzameling (`AppMeasurement.js`) en deze vervangen door de Web SDK JavaScript-bibliotheek (`alloy.js`).

## Voordelen en nadelen van dit implementatiepad

Het gebruiken van de uitbreiding van SDK van het Web om gegevens naar Adobe Analytics te verzenden heeft zowel voordelen als nadelen. Let zorgvuldig op elke optie om te bepalen welke benadering het beste is voor uw organisatie.

| Voordelen | Nadelen |
| --- | --- |
| <ul><li>**Meest directe benadering**: Dit implementatiepad is het meest ongecompliceerde en doorgaans het aanbevolen pad voor nieuwe Web SDK-implementaties. Als u geen huidige implementatie van Adobe Analytics om zich over ongerust te maken hebt, bevolk de toepasselijke gebieden van SDK van het Web XDM.</li><li>**Vooraf gedefinieerd schema**: Als uw organisatie geen behoefte aan uw eigen schema heeft, kunt u eenvoudig het schema gebruiken dat aan Adobe Analytics wordt gericht. Dit concept is zelfs van toepassing als u naar Customer Journey Analytics gaat. Het concept &#39;props&#39; en &#39;eVars&#39; zijn niet van toepassing op Customer Journey Analytics, maar u kunt &#39;props&#39; en &#39;eVars&#39; blijven gebruiken als eenvoudige aangepaste afmetingen.</li><li>**Tags beheren zonder tussenkomst van de ontwikkelaar**: Met labels kunt u uw implementatie beheren zonder dat ontwikkelaars hoeven aan te vragen dat ze code wijzigen in uw implementatie. Uw ontwikkelaars installeren het lader-script voor tags en u hebt volledige controle over de manier waarop gegevens worden verzameld.</li></ul> | <ul><li>**Vergrendeld in een specifiek schema**: Wanneer uw organisatie naar Customer Journey Analytics gaat, moet u het Adobe Analytics-schema blijven gebruiken of naar het schema van uw eigen organisatie migreren (wat een aparte gegevensset zou zijn). Als uw organisatie zowel het Adobe Analytics-schema als de migratie naar een aparte gegevensset bij de overgang naar de Customer Journey Analytics wil vermijden, raadt Adobe een van de volgende twee methoden aan:<ul><li>Gebruik de `data` object: Het `data` kunt u gegevens naar Adobe Analytics verzenden zonder aan een XDM-schema te voldoen. Zodra het schema van uw organisatie wordt gecreeerd, kunt u gegevenstoewijzing aan kaart gebruiken `data` objectvelden naar XDM. Beide [De uitbreiding van de Analyse aan de uitbreiding van SDK van het Web](analytics-extension-to-web-sdk.md) en [AppMeasurement naar Web SDK JavaScript-bibliotheek](appmeasurement-to-web-sdk.md) gebruiken `data` object.</li><li>Adobe Analytics volledig overslaan: als u de SDK van het Web implementeert, kunt u die gegevens naar een dataset in Adobe Experience Platform verzenden voor gebruik in Customer Journey Analytics. U kunt elk schema gebruiken dat u bevalt. Adobe Analytics is helemaal niet betrokken bij deze workflow en vereist daarom niet de Adobe Analytics ExperienceEvent-veldgroep. Deze methode leidt tot het minste bedrag aan technische schulden, maar laat Adobe Analytics ook volledig buiten beeld.</li></ul></ul> |


