---
title: Clienttips
description: Leer over hoe de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie zullen vervangen.
exl-id: e0a74daa-12a2-4999-9920-2636b061dcc8
feature: Data Configuration and Collection
role: Admin
source-git-commit: 43c39b99cbae3e714b7f017dec14dd02fa350790
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Overzicht van tips en veelgestelde vragen voor klanten

Clienttips zijn afzonderlijke informatie over het apparaat van een gebruiker. Deze worden geleverd door Chromium-browsers zoals Google Chrome en Microsoft Edge. Voor deze browsers, zullen de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie vervangen. Adobe Analytics zal zijn proces van de apparatenraadpleging bijwerken zodat het cliëntwenken naast gebruiker-Agent gebruikt om apparateninformatie te bepalen.

## Tips voor client met lage entropie en hoge entropie

Google verdeelt de gebruiker-Agent cliëntwenken in twee categorieën: laag-entropie en high-entropy wenken.

* **Hints met lage entropie** bevat meer generieke informatie over apparaten. Deze tips worden automatisch door Chromium-browsers geleverd.

* **Hoge entropie** de wenken bevatten meer gedetailleerde informatie. Deze tips zijn alleen op verzoek beschikbaar. Zowel AppMeasurement als Web SDK kunnen worden gevormd om high-entropy wenken te verzoeken. Beide bibliotheken doen dit standaard **niet** vragen om tips voor hoge entropie.

Vanaf oktober 2022 zijn nieuwe versies van Chromium-browsers begonnen met het &#39;bevriezen&#39; van de versie van het besturingssysteem die wordt weergegeven in de tekenreeks User-Agent. De versie van het besturingssysteem is een hoge entropiegelfunctie. Om de nauwkeurigheid van de versie van het besturingssysteem in uw rapportage te behouden, is het nodig dat u de verzamelingsbibliotheek configureert om deze hoge entropietpunten te verzamelen. In de loop van de tijd zal andere apparateninformatie van gebruiker-Agent worden bevroren, die cliëntwenken vereist om apparaat te handhaven rapporteert nauwkeurigheid.

De wenken van de cliënt zullen in het proces van de het apparatenraadpleging van Analytics van 27 februari 2023 en die op 2 maart 2023 worden opgenomen. Zowel AppMeasurement als Web SDK steunen momenteel inzameling van wenkengegevens maar het zal niet in apparatenraadpleging tot medio februari worden gebruikt. Zoals hieronder vermeld, werd de versie van het besturingssysteem vanaf oktober bevroren, maar dit was toe te schrijven aan een geleidelijke implementatie en het feit dat veel Gebruikersagenten al een bevroren versie van het besturingssysteem leveren (zie meer [hier](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html)), schatten wij dat dit &lt;3% van de bezoekers van Chrome zal beïnvloeden.

>[!NOTE]
>
> Vanaf januari 2023 worden sommige versies van Mac- en Windows-besturingssystemen onjuist weergegeven in de gebruikersagent, maar correct weergegeven in clienthints met hoge entropie. Zie [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html) voor meer informatie .

Adobe Audience Manager vereist dat hips met hoge entropiegels worden verzameld om de volledige functionaliteit te behouden. Als u [server-kant door:sturen aan Adobe Audience Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) dan kunt u inzameling van high-entropy wenken willen toelaten.

## Veelgestelde vragen

+++**Waar kan ik meer over cliëntwenken leren?**

Dit [Google-blogbericht](https://web.dev/user-agent-client-hints/) is een goede referentie en een goed uitgangspunt.

+++

+++**Hoe laat ik de inzameling van cliëntwenken toe?**

Tips voor lage entropie worden automatisch door de browser opgegeven en worden opgenomen om apparaat- en browserinformatie af te leiden. De nieuwere versies van Web SDK (die met 2.12.0 beginnen) en AppMeasurement (die met 2.23.0 beginnen) kunnen worden gevormd om hoge entropiegels via hun respectieve uitbreidingen van Markeringen of direct via een configuratieoptie te verzamelen. Zie aanwijzingen voor [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html#enabling-high-entropy-client-hints) en [AppMeasurement](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/collecthighentropyuseragenthints.html).

Voor beide bibliotheken is het verzamelen van hoge entropiehints **standaard uitgeschakeld**.

Voor gegevens die via API worden verzonden, bijvoorbeeld via [API voor gegevensinvoer](https://github.com/AdobeDocs/analytics-1.4-apis/blob/master/docs/data-insertion-api/index.md) of [API voor het invoegen van bulkgegevens](https://experienceleague.adobe.com/docs/analytics/import/bulk-data-insert.html), moeten tips expliciet in de lading worden opgenomen. Zie de desbetreffende documentatie voor meer informatie.

+++

+++**Kan ik kiezen welke hoge entropips ik verzamel?**

Op dit moment niet. U kunt ervoor kiezen alle hints met hoge entropie of geen hints te verzamelen.

fullVersionList wordt momenteel niet verzameld omdat de hoofdversie van de browser wordt vastgelegd als een low-entropy hint.

+++

+++**Wat zijn de verschillende waarden van de cliëntwenken?**

In de onderstaande tabel worden de tips voor cliënten vanaf oktober 2022 beschreven.

| Tip | Beschrijving | Hoog of laag | Voorbeeld |
| --- | --- | --- | --- | 
| Sec-CH-UA | Browser en significante versie | Laag | `"Google Chrome 84"` |
| Sec-CH-UA-Mobile | Mobiel apparaat (true of false) | Laag | `true` |
| Sec-CH-UA-Platform | Besturingssysteem/platform | Laag | `"Android"` |
| architectuur | Architectuur van de site | Hoog | `"arm"` |
| bittheid | Bitsheid van architectuur | Hoog | `"64"` |
| fullVersionList | Lijst van merken met hun versie | Hoog | `"Not A;Brand";v="99", "Chromium";v="98", "Google Chrome";v="98"` |
| model | Apparaatmodel | Hoog | `"Pixel 3"` |
| platformVersion | Besturingssysteem/platformversie | Hoog | `"10"` |

* Hints met lage entropie worden verzameld via de aanvraagkoptekst.
* Hoog-entropiewenken worden verzameld door JavaScript en door de parameterwaarden van het vraagkoord overgegaan. De parameters van het vraagkoord gebruiken `h.` als voorvoegsel in de afbeeldingsaanvraag. fullVersionList wordt momenteel niet verzameld omdat de hoofdversie van de browser wordt vastgelegd als een lage entropiehint.

Hoge entropiehints worden verzameld via JavaScript-aanroep en doorgegeven via queryparameter

+++

+++**Worden er wijzigingen aangebracht in apparaatrapportage in Analytics?**

De beschikbare apparaatvelden voor rapportage blijven ongewijzigd. De gegevens die voor die velden worden vastgelegd, kunnen veranderen afhankelijk van welk veld en hoe u verzameling voor clienttips hebt geconfigureerd.

+++

+++**Welke Analytics rapporterend gebieden worden afgeleid uit gebruiker-Agent?**

Deze gebieden worden direct afgeleid uit gebruiker-Agent maar user-Agent kan worden gebruikt om waarden voor andere apparaat verwante gebieden af te leiden, afhankelijk van de apparatendetails.

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html)
* [Browsertype](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html)
* [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html)
* [Typen besturingssystemen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html)
* [Mobiel apparaat en type mobiel apparaat](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html)

+++

+++**Welke gedeelten van de user-Agent worden &quot;bevroren&quot;en wanneer?**

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dit kan worden gewijzigd.

+++

+++**Op welke manieren is Analytics afhankelijk van de Gebruikersagent?**

Apparaatinformatie in rapportage wordt afgeleid van de gebruikersagent. Wij hebben onze processen bijgewerkt om zowel de Agent van de Gebruiker als cliëntwenken te gebruiken waar beschikbaar.

De fallback-id ([s_fid](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/analytics-ids.html)) wordt afgeleid uit de Agent van de Gebruiker en IP Adres. Deze id wordt alleen gebruikt als een cookie niet kan worden ingesteld en daarom niet op grote schaal wordt gebruikt

+++

+++**Welke analytische rapporteringsgebieden worden afgeleid van waarden die in hoge entropiewenken worden opgeslagen?**

Dit zal in tijd veranderen aangezien Google meer delen van de Gebruikersagent &quot;bevriest&quot;. Het eerste veld dat rechtstreeks moet worden beïnvloed, is &quot;Besturingssysteem&quot;, dat de versie van het besturingssysteem bevat Volgens de gepubliceerde tijdlijn van Google voor &quot;bevriezen&quot; van gebruikers-agent-tips, wordt de versie van het besturingssysteem vanaf eind oktober 2022 bevroren met Chromium versie 107. Op dat moment is de versie van het besturingssysteem in de gebruikersagent in sommige gevallen niet correct.

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) om de timing voor het bevriezen van andere gedeelten van user-Agent te zien.

+++

+++**Hoe zal de Adobe cliëntwenken gebruiken om apparateninformatie af te leiden?**

De Adobe gebruikt een derde, Atlas van het Apparaat, die zowel cliëntwenken als gebruiker-Agent zal gebruiken om apparateninformatie af te leiden.

+++

+++**Welke browsers worden beïnvloed door cliëntwenken?**

Clienttips zijn alleen van toepassing op Chromium-browsers zoals Google Chrome en Microsoft Edge. Er is geen wijziging in de gegevens van andere browsers of mobiele apps.

+++

+++**Worden de cliëntwenken gesteund over onveilige verbindingen?**

Nee. Clienttips kunnen alleen worden verzameld via een beveiligde HTTP-verbinding, zoals HTTPS.

+++

+++**Hoe kan ik gegevens voor clienttips opnemen bij het gebruik van API-verzending?**

Zie documentatie voor het opnemen van deze via [API voor het invoegen van bulkgegevens](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/file-format/).

+++

+++**Zijn de cliëntwenken beschikbaar in gegevens die naar Adobe Experience Platform en Customer Journey Analytics via de Bron van de Adobe schakelaar worden verzonden?**

De Adobe is van plan om cliëntwenken in gegevens via de Schakelaar van de Bron van de Adobe in de eerste helft van 2023 te omvatten.

+++

+++**Hoe worden cliëntwenken vertegenwoordigd in XDM?**

Zie de [schemadocumentatie](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Zal Adobe Audience Manager server-kant het door:sturen cliëntwenken steunen?**

Ja. Clienttips worden opgenomen in de gegevens die naar Adobe Audience Manager worden doorgestuurd. Adobe Audience Manager vereist dat hips met hoge entropiegels worden verzameld om de volledige functionaliteit te behouden. Als u [server-kant door:sturen aan Adobe Audience Manager](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) dan kunt u inzameling van high-entropy wenken willen toelaten.

+++
