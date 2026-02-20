---
title: bezoekerID
description: Gebruik een aangepaste bezoeker-id.
feature: Appmeasurement Implementation
exl-id: cb336042-01a1-4a66-a947-a221a7919c1b
role: Admin, Developer
source-git-commit: de98bf68c57f5453b6662f6e6e57312d8fd3e642
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# bezoekerID

Adobe gebruikt verscheidene verschillende methodes om bezoekers [&#x200B; op uw plaats te identificeren &#x200B;](../../id/overview.md). **de `visitorID` variabele treedt alle andere methodes van bezoekersidentificatie met voeten.**

>[!IMPORTANT]
>
>Adobe raadt u af deze variabele te gebruiken. Gebruik in plaats hiervan de [&#x200B; Dienst van de Identiteit van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html).

## Hoe Analytics gebruikt `visitorID`

Deze variabele is een handmatige ID-overschrijving van de bezoeker die alle andere vormen van bezoekersidentificatie vervangt. Om als één enkele bezoeker te worden geteld, moet elke klap voor een persoon de zelfde `visitorID` waarde gebruiken.

* Hiermee geeft u `visitorID` weer wanneer u een bezoeker identificeert, en wordt u beschouwd als een aparte bezoeker.
* Punten die meer dan een `visitorID` -waarde gebruiken, worden als aparte bezoekers beschouwd.
* Adobe hecht geen treffers die verschillende bezoekers-id&#39;s samen gebruiken.

Zie [&#x200B; identificatie van de Bezoeker in Adobe Analytics &#x200B;](../../id/overview.md) voor details op identificatieprioriteit en waarom het mengen van herkenningstekens bezoekerscijfers kan opblazen.

>[!WARNING]
>
>Stel `visitorID` alleen in als u kunt garanderen dat de waarde bij elke treffer voor die persoon is ingesteld en dat de waarde nooit wordt gewijzigd. Als u deze optie alleen instelt op bepaalde treffers, deze introduceert tijdens een bezoek (bijvoorbeeld bij verificatie) of wijzigt tussen hits, wordt de activiteit van één bezoeker opgesplitst in meerdere bezoekers.

>[!CAUTION]
>
>Ongeldige waarden voor de aangepaste bezoeker-id kunnen leiden tot onjuiste gegevens en slechte rapportprestaties. Als deze variabele een standaardwaarde of plaatsaanduidingswaarde bevat (zoals `"0"` of `"NULL"` ), behandelt Adobe deze treffers alsof ze dezelfde bezoeker zijn. Deze situatie leidt tot onjuiste gegevens, waarbij het aantal bezoekers kunstmatig laag is en de segmenten op bezoekersniveau niet naar behoren werken. Incorrect uitgevoerde douaneIDs van de bezoeker kan zware lading op verwerkingsservers ook introduceren, die [&#x200B; latentie &#x200B;](/help/technotes/latency.md) verhogen en rapportprestaties verminderen.

## Bezoeker-id met de Adobe Analytics-extensie

[!UICONTROL Visitor ID] is een veld onder de accordeon van [!UICONTROL Cookies] wanneer u de Adobe Analytics-extensie configureert.

1. Login aan [&#x200B; de Inzameling van Gegevens van Adobe Experience Platform &#x200B;](https://experience.adobe.com/data-collection) gebruikend uw geloofsbrieven van AdobeID.
2. Selecteer de gewenste eigenschap tag.
3. Ga naar de tab [!UICONTROL Extensions] en selecteer vervolgens de knop **[!UICONTROL Configure]** onder Adobe Analytics.
4. Vouw de accordeon [!UICONTROL Cookies] uit, zodat het veld [!UICONTROL Visitor ID] zichtbaar wordt.

Wijs dit veld toe aan het gegevenselement dat uw aangepaste bezoeker-id bevat. **plaats dit gebied niet aan één enkele statische waarde voor alle bezoekers.** Gebruik een gegevenselement dat per bezoeker oplost en voor alle treffers constant blijft.

## s.bezoekerID in AppMeasurement en de de coderedacteur van de uitbreiding van de Analyse

De variabele `s.visitorID` is een tekenreeks die een aangepaste unieke id voor de bezoeker bevat. Geldige waarden zijn alfanumerieke tekens tot 100 bytes. Gebruik geen streepjes, spaties, onderstrepingstekens of symbolen in deze variabele.

```js
s.visitorID = "abc123";
```

## Bezoeker-id met de Web SDK

Adobe Experience Platform Edge Network staat u toe om veelvoudige herkenningstekens te verstrekken gebruikend de Kaart van de Identiteit XDM [&#x200B; &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/edge/identity/overview.html#using-identitymap). Elke identiteit in een identiteitskaart heeft een verschillende namespace. U kunt specificeren welke namespace voor bezoekersidentiteitskaart als deel van [&#x200B; gegevensstroomconfiguratie &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/datastreams/configure.html#analytics) zou moeten worden gebruikt. Zodra dit gebied wordt gevormd, wanneer u een gebeurtenis met een waarde verzendt die voor dit namespace wordt gespecificeerd, wordt het automatisch gebruikt als bezoekersidentiteitskaart in Analytics.
