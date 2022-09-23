---
title: Clienttips
description: Leer over hoe de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie zullen vervangen.
source-git-commit: cd8370f6c19e79e1a8a506e772db390708e96a44
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 2%

---


# Overzicht van tips en veelgestelde vragen voor klanten

Clienttips zijn afzonderlijke informatie over het apparaat van een gebruiker. Deze worden geleverd door Chromium-browsers zoals Google Chrome en Microsoft Edge. Voor deze browsers, zullen de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie vervangen. Adobe Analytics zal zijn proces van de apparatenraadpleging bijwerken zodat het cliëntwenken naast gebruiker-Agent gebruikt om apparateninformatie te bepalen.

Google verdeelt gebruikers-Agent-clienttips in twee categorieën: een lage entropie en hoge entropiehints.

* Lage entropiehints bevatten meer algemene informatie over apparaten. Deze tips worden automatisch door Chromium-browsers geleverd.

* Hoog-entropiewenken hebben meer gedetailleerde informatie. Deze tips zijn alleen op aanvraag beschikbaar. Zowel kunnen AppMeasurement als Web SDK worden gevormd om high-entropy wenken te verzoeken. Beide bibliotheken doen dit standaard **niet** vragen om tips voor hoge entropie.

>[!NOTE]
>
>Vanaf oktober 2022 starten nieuwe versies van Chromium-browsers de versie van het besturingssysteem die wordt weergegeven in de tekenreeks User-Agent, &#39;bevriezen&#39;. Wanneer gebruikers hun apparaten upgraden, verandert het besturingssysteem in de gebruikersagent niet. Zo, in tijd zal de werkende versieinformatie zoals die in gebruiker-Agent wordt vertegenwoordigd minder nauwkeurig worden. De versie van het besturingssysteem is een hoge entropiegelfunctie. Om de nauwkeurigheid van de versie van het besturingssysteem in uw rapportage te behouden, is het nodig dat u de verzamelingsbibliotheek configureert om deze hoge entropietpunten te verzamelen. In de loop van de tijd zal andere apparateninformatie van gebruiker-Agent worden bevroren, die cliëntwenken vereist om apparaat te handhaven rapporteert nauwkeurigheid.

## Veelgestelde vragen

+++**Waar kan ik meer over cliëntwenken leren?**

Dit [Google-blogbericht](https://web.dev/user-agent-client-hints/) is een goede referentie en een goed uitgangspunt.

+++

+++**Hoe laat ik de inzameling van cliëntwenken toe?**

Lage-entrophints worden automatisch door de browser verstrekt en opgenomen in Adobe proces voor het afleiden van apparaat en browser informatie. De nieuwere versies van AppMeasurement (die met 2.23.0 begint) en Web SDK (die met 2.12.0 begint) kunnen worden gevormd om high-entropy wenken te verzamelen. Voor beide bibliotheken is het verzamelen van hoge entropiehints **standaard uitgeschakeld**.

+++

+++**Hoe leg ik hoge entropiehints vast?**

Hoog-entropy wenken kunnen met de bibliotheken van SDK van het Web en van AppMeasurement via hun respectieve uitbreidingen van Markeringen of direct met de collectiefHighEntropyUserAgentHints vlag worden gevormd.

+++

+++**Kan ik kiezen welke hoge entropips ik verzamel?**

Op dit moment niet. U kunt ervoor kiezen alle hints met hoge entropie of geen hints te verzamelen.

+++

+++**Worden er wijzigingen aangebracht in apparaatrapportage in Analytics?**

De beschikbare apparaatvelden voor rapportage blijven ongewijzigd. De gegevens die voor die velden worden vastgelegd, kunnen veranderen afhankelijk van welk veld en hoe u verzameling voor clienttips hebt geconfigureerd.

+++

+++**Welke Analytics rapporterend gebieden worden afgeleid uit gebruiker-Agent?**

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [Browsertype](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [Typen besturingssystemen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [Mobiel apparaat en type mobiel apparaat](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)
* [Gegevensfeeds](https://experienceleague.adobe.com/docs/analytics/export/analytics-data-feed/data-feed-contents/datafeeds-reference.html?lang=en)

+++

+++**Welke analytische rapporteringsgebieden worden afgeleid van waarden die in hoge entropiewenken worden opgeslagen?**

Vanaf september 2022 geeft de door Google gepubliceerde tijdlijn voor het &quot;bevriezen&quot; van gebruikers-agent aan dat de versie van het besturingssysteem vanaf oktober 2022 niet meer wordt bijgewerkt. Wanneer gebruikers hun besturingssysteem upgraden, wordt de versie van het besturingssysteem in de User-Agent niet bijgewerkt. Zonder hoge entropiegels zal de nauwkeurigheid van de versie van het besturingssysteem, die deel uitmaakt van de dimensie &quot;Besturingssysteem&quot; van Analytics, geleidelijk afnemen.

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) om de timing voor het bevriezen van andere gedeelten van user-Agent te zien.

+++

+++**Hoe zal Adobe cliëntwenken gebruiken om apparateninformatie af te leiden?**

Adobe gebruikt een derde, de Atlas van het Apparaat, die zowel de cliëntwenken als gebruiker-Agent zal gebruiken om apparateninformatie af te leiden.

+++

+++**Welke browsers worden beïnvloed door cliëntwenken?**

Clienttips zijn alleen van toepassing op Chromium-browsers zoals Google Chrome en Microsoft Edge. Er is geen wijziging in de gegevens van andere browsers of mobiele apps.

+++

+++**Zijn de cliëntwenken beschikbaar in gegevens die naar AEP en CJA via de Bron van de Adobe schakelaar worden verzonden?**

We zijn van plan om in de eerste helft van 2023 client-tips op te nemen in gegevens via Adobe Source Connector.

+++

+++**Hoe worden cliëntwenken vertegenwoordigd in XDM?**

Zie de [schemadocumentatie](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Wat zijn de verschillende gebieden van de wenk? Welke hebben invloed op apparaatrapportage?**

In de onderstaande tabel worden de tips voor cliënten vanaf september 2022 beschreven.

| Tip | Beschrijving | Hoog of laag | Voorbeeld |
| --- | --- | --- | --- | 
| Sec-CH-UA | Browser en significante versie | Laag | &quot;Google Chrome 84&quot; |
| Sec-CH-UA-Mobile | Mobiel apparaat (true of false) | Laag | TRUE |
| Sec-CH-UA-Platform | Besturingssysteem/Platform | Laag | &quot;Android&quot; |
| Sec-CH-UA-Arch | Architectuur van de site | Hoog | &quot;arm&quot; |
| Sec-CH-UA-Bitness | Architectuurbitnes | Hoog | &quot;64&quot; |
| Sec-CH-UA-Full-Version | Volledige versie van de browser | Hoog | &quot;84.0.4143.2&quot; |
| Sec-CH-UA-Full-Version-List | Lijst van merken met hun versie | Hoog | &quot;Not A;Brand&quot;;v=&quot;99&quot;, &quot;Chromium&quot;;v=&quot;98&quot;, &quot;Google Chrome&quot;;v=&quot;98&quot; |
| Sec-CH-UA-model | Apparaatmodel | Hoog | &quot;Pixel 3&quot; |
| Sec-CH-UA-Platform-Version | Versie besturingssysteem/Platform | Hoog | &quot;10&quot; |

+++



+++**Welke gedeelten van de user-Agent worden &quot;bevroren&quot;en wanneer?**

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dit kan worden gewijzigd.

+++
