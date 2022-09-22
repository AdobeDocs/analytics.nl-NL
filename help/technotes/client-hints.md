---
title: Clienttips
description: Meer informatie over
source-git-commit: b99852f4b8e0a3034ea8965e5646b1ab2f1a8c4c
workflow-type: tm+mt
source-wordcount: '889'
ht-degree: 2%

---


# Overzicht van tips en veelgestelde vragen voor klanten

Clienttips zijn afzonderlijke informatie over het apparaat van een gebruiker. Deze worden geleverd door Chromium-browsers zoals Google Chrome en Microsoft Edge. Voor deze browsers, zullen de cliëntwenken geleidelijk de Agent van de Gebruiker als bron van apparateninformatie vervangen. Adobe Analytics werkt het opzoekproces van het apparaat bij, zodat het naast Gebruikersagent ook clienttips gebruikt om apparaatinformatie te bepalen.

Google verdeelt de clienttips van de gebruikersagent in twee categorieën: een lage entropie en hoge entropiehints.

* Lage entropiehints bevatten meer algemene informatie over apparaten. Deze tips worden automatisch door Chromium-browsers geleverd.

* Hoog-entropiewenken hebben meer gedetailleerde informatie. Deze tips zijn alleen op aanvraag beschikbaar. Zowel kunnen AppMeasurement als Web SDK worden gevormd om high-entropy wenken te verzoeken. Beide bibliotheken doen dit standaard **niet** vragen om tips voor hoge entropie.

>[!NOTE]
>
>Vanaf oktober 2022 starten nieuwe versies van Chromium-browsers het &#39;bevriezen&#39; van de versie van het besturingssysteem die wordt weergegeven in de tekenreeks Gebruikersagent. Dit betekent dat, in tijd, de informatie van de werkende versie zoals vertegenwoordigd in de Agent van de Gebruiker minder nauwkeurig zal worden. De versie van het besturingssysteem is een hoge entropiegelfunctie. Om de nauwkeurigheid van de versie van het besturingssysteem in uw rapportage te behouden, is het nodig dat u de verzamelingsbibliotheek configureert om deze hoge entropietpunten te verzamelen. In de loop der tijd wordt andere apparaatinformatie van de gebruikersagent bevroren, waardoor de client hints vereist zijn om de nauwkeurigheid van apparaatrapportage te behouden.

## Veelgestelde vragen

+++**Hoe laat ik de inzameling van cliëntwenken toe?**

Lage-entrophints worden automatisch door de browser verstrekt en in het proces van Adobe voor apparateninformatie inbegrepen. De nieuwere versies van AppMeasurement (beginnend TBD) en Web SDK (beginnend TBD) kunnen worden gevormd om high-entropy wenken te verzamelen. Voor beide bibliotheken is het verzamelen van hoge entropiehints **standaard uitgeschakeld**. Zie hier voor meer informatie over hoe u dit kunt implementeren.

+++**Kan ik kiezen welke hoge entropips ik verzamel?**

Op dit moment niet. U kunt ervoor kiezen alle hints met hoge entropie of geen hints te verzamelen.

+++**Worden er wijzigingen aangebracht in apparaatrapportage in Analytics?**

De beschikbare apparaatvelden voor rapportage blijven ongewijzigd. De gegevens die voor die gebieden worden gevangen kunnen veranderen afhankelijk van welk gebied en hoe u inzameling voor cliëntwenken hebt gevormd.

+++**Welke Analytics rapporterend gebieden worden afgeleid uit de Agent van de Gebruiker?**

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [Browsertype](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [Typen besturingssystemen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [Mobiel apparaat en type mobiel apparaat](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)??
* Gegevensfeeds (gebruikers moeten bijwerken om deze velden vast te leggen. Bovendien is er een afhankelijkheid waarbij mobiele id niet samen met apparaatinformatie toegankelijk kan worden gemaakt.)
* Bronverbinding voor analyse (niet gereed)

+++**Welke analytische rapporteringsgebieden worden afgeleid van waarden die in hoge entropiewenken worden opgeslagen?**

Vanaf september 2022 geeft de door Google gepubliceerde tijdlijn voor het bevriezen van gebruikers-agent-tips aan dat de versie van het besturingssysteem vanaf oktober 2022 niet meer wordt bijgewerkt. Zonder hoge entropiehints zal de nauwkeurigheid van de versie van het besturingssysteem, die is opgenomen in de dimensie &quot;Besturingssysteem&quot; van Analytics, geleidelijk afnemen.

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) om de timing voor het bevriezen van de gebruikersagent te zien.

+++**Welke browsers worden beïnvloed door cliëntwenken?**

Clienttips zijn alleen van toepassing op Chromium-browsers zoals Google Chrome en Microsoft Edge. Er is geen wijziging in de gegevens van andere browsers of mobiele apps.

+++**Hoe zal Adobe cliëntwenken gebruiken om apparateninformatie af te leiden?**

Adobe gebruikt een derde, de Atlas van het Apparaat, die zowel de cliëntwenken als gebruikersagent zal gebruiken om apparateninformatie af te leiden.

+++**Zullen de cliëntwenken in gegevensvoer beschikbaar zijn?**

Ja. Zie de documentatie (voor verdere informatie).

+++**Zijn de cliëntwenken beschikbaar in gegevens die naar AEP en CJA via de Bron van de Adobe schakelaar worden verzonden?**

We zijn van plan om in de eerste helft van 2023 client-tips op te nemen in gegevens via Adobe Source Connector.

+++**Hoe worden cliëntwenken vertegenwoordigd in XDM?**

Zie de [schemadocumentatie](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++**Waar kan ik meer over cliëntwenken leren?**

Dit [Google-blogbericht](https://web.dev/user-agent-client-hints/) is een goede referentie en een goed uitgangspunt.

+++**Wat zijn de verschillende gebieden van de wenk? Welke hebben invloed op apparaatrapportage?**

In de onderstaande tabel worden de tips voor cliënten vanaf september 2022 beschreven.

| Tip (koptekst) | Tip | Hoog of laag | Voorbeeld | Analyses die velden rapporteren |
| --- | --- | --- | --- | --- |
| Sec-CH-UA | Browser en significante versie | Laag | Google Chrome 84 | [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en) en [Browsertype](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en) |
| Sec-CH-UA-Mobile | Mobiel apparaat (true of false) | Laag | TRUE | [Mobiel apparaat en type mobiel apparaat](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)?? |
| Sec-CH-UA-Platform | Besturingssysteem/Platform | Laag | Android | [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en) |
| Sec-CH-UA-Arch | Architectuur van de site | Hoog | &quot;arm&quot; | Geen? |
| Sec-CH-UA-Bitness | Sec-CH-UA-Bitness | Hoog |  | Geen? |
| Sec-CH-UA-Full-Version | Volledige versie van de browser | Hoog | &quot;84.0.4143.2&quot; | Geen? |
| Sec-CH-UA-Full-Version-List | ??? | Hoog | ??? | Geen? |
| Sec-CH-UA-model | Apparaatmodel | Hoog | &quot;Pixel 3&quot; | Geen? |
| Sec-CH-UA-Platform-Version | Versie besturingssysteem/Platform | Hoog | &quot;10&quot; | [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en) |

+++**Hoe leg ik hoge entropiehints vast?**

Hoog-entropiewenken kunnen worden gevormd

* Rechtstreeks voor AppMeasurement [koppeling naar markeeritem in implementatiegids]
* In de extensie Tags Analytics
* In het Web SDK.

+++**Welke gegevens worden verwijderd uit de Gebruikersagent en wanneer?**

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dit kan worden gewijzigd.

+++