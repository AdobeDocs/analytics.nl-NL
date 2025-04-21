---
title: Clienttips
description: Leer over hoe de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie zullen vervangen.
exl-id: e0a74daa-12a2-4999-9920-2636b061dcc8
feature: Data Configuration and Collection
role: Admin
source-git-commit: 73c0210ac931f3e7f823e033a3bffdc22e159ddb
workflow-type: tm+mt
source-wordcount: '1184'
ht-degree: 0%

---

# Overzicht van tips en veelgestelde vragen voor klanten

Clienttips zijn afzonderlijke informatie over het apparaat van een gebruiker. Ze worden geleverd door Chromium-browsers zoals Google Chrome en Microsoft Edge. Voor deze browsers, zullen de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie vervangen. Adobe Analytics zal zijn proces van de apparatenraadpleging bijwerken zodat het cliëntwenken naast gebruiker-Agent gebruikt om apparateninformatie te bepalen.

## Tips voor client met lage entropie en hoge entropie

Google verdeelt de gebruiker-Agent cliëntwenken in twee categorieën: laag-entropie en high-entropy wenken.

* **Lage-entropy wenken** bevatten meer generische informatie over apparaten. Deze tips worden automatisch door Chromium-browsers geleverd.

* **Hoog-entropie** wenken bevatten meer gedetailleerde informatie. Deze tips zijn alleen op verzoek beschikbaar. Zowel AppMeasurement als Web SDK kunnen worden geconfigureerd om tips voor hoge entropie aan te vragen. Door gebrek, vragen beide bibliotheken **** geen high-entropy wenken.

Vanaf oktober 2022 zijn nieuwe versies van Chromium-browsers begonnen met het &#39;bevriezen&#39; van de versie van het besturingssysteem die wordt weergegeven in de tekenreeks User-Agent. De versie van het besturingssysteem is een hoge entropiegelfunctie. Om de nauwkeurigheid van de versie van het besturingssysteem in uw rapportage te behouden, is het nodig dat u de verzamelingsbibliotheek configureert om deze hoge entropietpunten te verzamelen. In de loop van de tijd zal andere apparateninformatie van gebruiker-Agent worden bevroren, die cliëntwenken vereist om apparaat te handhaven rapporteert nauwkeurigheid.

De wenken van de cliënt zullen in het proces van de het apparatenraadpleging van Analytics van 27 februari 2023 en die op 2 maart 2023 worden opgenomen. Zowel AppMeasurement als Web SDK steunen momenteel inzameling van wenkengegevens maar het zal niet in apparatenraadpleging tot medio februari worden gebruikt. Zoals vermeld onder werkende systeemversie werd bevroren die in Oktober maar wegens een geleidelijke uitrol begint en het feit dat vele Medewerkers van de Gebruiker reeds een bevroren OS versie (zie meer [ hier ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html)) verstrekken, schatten wij dat dit &lt;3% van Bezoekers van Chrome zal beïnvloeden.

>[!NOTE]
>
> Vanaf januari 2023 worden sommige versies van Mac- en Windows-besturingssystemen onjuist weergegeven in de gebruikersagent, maar correct weergegeven in clienthints met hoge entropie. Zie [ Werkend Systeem ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html) voor meer informatie.

Adobe Audience Manager vereist dat hips met hoge entropiegels worden verzameld om de volledige functionaliteit te behouden. Als u [ server-kant het door:sturen aan Adobe Audience Manager ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) gebruikt dan kunt u inzameling van high-entropy wenken willen toelaten.

## Veelgestelde vragen

+++**waar kan ik meer over cliëntwenken leren?**

Dit [ de blogpost van Google ](https://web.dev/user-agent-client-hints/) is een goede verwijzing en een uitgangspunt.

+++

+++**Hoe laat ik de inzameling van cliëntwenken toe?**

Tips voor lage entropie worden automatisch door de browser opgegeven en worden opgenomen om apparaat- en browserinformatie af te leiden. Nieuwere versies van Web SDK (vanaf 2.12.0) en AppMeasurement (vanaf 2.23.0) kunnen worden geconfigureerd voor het verzamelen van hoge entropiehints via hun respectievelijke Tags-extensies of rechtstreeks via een configuratieoptie. Zie richtingen voor [ SDK van het Web ](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html#enabling-high-entropy-client-hints) en [ AppMeasurement ](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/collecthighentropyuseragenthints.html).

Voor beide bibliotheken, wordt de inzameling van high-entropy wenken **onbruikbaar gemaakt door gebrek**.

Voor gegevens die via API worden voorgelegd, zoals via [ de Invoeging API van Gegevens ](https://developer.adobe.com/analytics-apis/docs/1.4/guides/data-insertion/) of [ Bulk API van de Invoeging van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/), moeten de wenken uitdrukkelijk inbegrepen in de nuttige lading zijn. Zie de desbetreffende documentatie voor meer informatie.

+++

+++**kan ik kiezen welke high-entropy wenken ik verzamel?**

Op dit moment niet. U kunt ervoor kiezen alle hints met hoge entropie of geen hints te verzamelen.

fullVersionList wordt momenteel niet verzameld omdat de hoofdversie van de browser wordt vastgelegd als een low-entropy hint.

+++

+++**wat zijn de diverse waarden van cliëntwenken?**

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
* Hoog-entropy wenken worden verzameld door JavaScript en door de parameterwaarden van het vraagkoord overgegaan. De parameters van de queryreeks gebruiken `h.` als voorvoegsel in de afbeeldingsaanvraag. fullVersionList wordt momenteel niet verzameld omdat de hoofdversie van de browser wordt vastgelegd als een lage entropiehint.

Hoog entropingstips worden verzameld via JavaScript-aanroep en doorgegeven via queryparameter

+++

+++**zullen er om het even welke veranderingen aan apparaat rapporterend in Analytics zijn?**

De beschikbare apparaatvelden voor rapportage blijven ongewijzigd. De gegevens die voor die velden worden vastgelegd, kunnen veranderen afhankelijk van welk veld en hoe u verzameling voor clienttips hebt geconfigureerd.

+++

+++**Welke Analytics rapporterend gebieden worden afgeleid uit gebruiker-Agent?**

Deze gebieden worden direct afgeleid uit gebruiker-Agent maar user-Agent kan worden gebruikt om waarden voor andere apparaat verwante gebieden af te leiden, afhankelijk van de apparatendetails.

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html)
* [ Browser Type ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html)
* [ Werkend Systeem ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html)
* [Typen besturingssystemen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html)
* [ Mobiel Apparaat en Mobiel Type van Apparaat ](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html)

+++

+++**Welke gedeelten van gebruiker-Agent &quot;bevroren&quot;en wanneer worden?**

Zie de [ chronologie die door Google ](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) wordt gepubliceerd. Dit kan worden gewijzigd.

+++

+++**op welke manieren hangt Analytics van de Agent van de Gebruiker af?**

Apparaatinformatie in rapportage wordt afgeleid van de gebruikersagent. Wij hebben onze processen bijgewerkt om zowel de Agent van de Gebruiker als cliëntwenken te gebruiken waar beschikbaar.

Identiteitskaart van de Fallback ([ s_fid ](https://experienceleague.adobe.com/docs/id-service/using/reference/analytics-reference/analytics-ids.html)) wordt afgeleid uit de Agent van de Gebruiker en IP Adres. Deze id wordt alleen gebruikt als een cookie niet kan worden ingesteld en daarom niet op grote schaal wordt gebruikt

+++

+++**Welke Analytics rapporterend gebieden worden afgeleid uit waarden die in high-entropy wenken worden opgeslagen?**

Dit zal in tijd veranderen aangezien Google meer delen van de Gebruikersagent &quot;bevriest&quot;. Het eerste veld dat rechtstreeks moet worden beïnvloed, is &quot;Besturingssysteem&quot;, dat de versie van het besturingssysteem bevat Volgens de gepubliceerde tijdlijn van Google voor &quot;bevriezen&quot; van gebruikers-agent-tips, wordt de versie van het besturingssysteem vanaf eind oktober 2022 bevroren met Chromium versie 107. Op dat moment is de versie van het besturingssysteem in de gebruikersagent in sommige gevallen niet correct.

Verwijs naar de [ chronologie die door Google ](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) wordt gepubliceerd om de timing voor het bevriezen van andere gedeelten van gebruiker-Agent te zien.

+++

+++**hoe Adobe cliëntwenken zal gebruiken om apparateninformatie af te leiden?**

Adobe gebruikt een derde partij, de Atlas van het Apparaat, die zowel cliëntwenken als gebruiker-Agent zal gebruiken om apparateninformatie af te leiden.

+++

+++**Welke browsers worden beïnvloed door cliëntwenken?**

Clienttips zijn alleen van toepassing op Chromium-browsers zoals Google Chrome en Microsoft Edge. Er is geen wijziging in de gegevens van andere browsers of mobiele apps.

+++

+++**worden de cliëntwenken gesteund over onveilige verbindingen?**

Nee. Clienttips kunnen alleen worden verzameld via een beveiligde HTTP-verbinding, zoals HTTPS.

+++

+++**hoe ik gegevens van de cliëntwenk wanneer het gebruiken van API voorlegging?**

Zie documentatie voor het omvatten van deze via [ Bulk API van de Invoeging van Gegevens ](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/file-format/).

+++

+++**zal de cliëntwenken beschikbaar in gegevens zijn die naar Adobe Experience Platform en Customer Journey Analytics via de Verbinding van Adobe Source worden verzonden?**

Adobe is van plan om in de eerste helft van 2023 tips voor klanten op te nemen via Adobe Source Connector.

+++

+++**hoe worden de cliëntwenken vertegenwoordigd in XDM?**

Zie de [ schemadocumentatie ](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**zal Adobe Audience Manager server-kant door:sturen de wenken van de steuncliënt?**

Ja. Clienttips worden opgenomen in de gegevens die naar Adobe Audience Manager worden doorgestuurd. Adobe Audience Manager vereist dat hips met hoge entropiegels worden verzameld om de volledige functionaliteit te behouden. Als u [ server-kant het door:sturen aan Adobe Audience Manager ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) gebruikt dan kunt u inzameling van high-entropy wenken willen toelaten.

+++
