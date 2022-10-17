---
title: Clienttips
description: Leer over hoe de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie zullen vervangen.
source-git-commit: 9dfeb0f5cc3bb488fa28fb0d21c6969dfdfc9ef6
workflow-type: tm+mt
source-wordcount: '1073'
ht-degree: 1%

---


# Overzicht van tips en veelgestelde vragen voor klanten

Clienttips zijn afzonderlijke informatie over het apparaat van een gebruiker. Deze worden geleverd door Chromium-browsers zoals Google Chrome en Microsoft Edge. Voor deze browsers, zullen de cliëntwenken geleidelijk gebruiker-Agent als bron van apparateninformatie vervangen. Adobe Analytics zal zijn proces van de apparatenraadpleging bijwerken zodat het cliëntwenken naast gebruiker-Agent gebruikt om apparateninformatie te bepalen.

Google verdeelt gebruikers-Agent-clienttips in twee categorieën: een lage entropie en hoge entropiehints.

* **Hints met lage entropie** bevat meer generieke informatie over apparaten. Deze tips worden automatisch door Chromium-browsers geleverd.

* **Hoge entropie** de wenken bevatten meer gedetailleerde informatie. Deze tips zijn alleen op aanvraag beschikbaar. Zowel kunnen AppMeasurement als Web SDK worden gevormd om high-entropy wenken te verzoeken. Beide bibliotheken doen dit standaard **niet** vragen om tips voor hoge entropie.

>[!NOTE]
>
>De wenken van de cliënt zullen in het proces van de het apparatenraadpleging van Analytics vanaf medio Januari 2023 worden opgenomen. Zowel steunen AppMeasurement als Web SDK momenteel inzameling van wendengegevens maar het zal niet in apparatenraadpleging tot medio januari worden gebruikt. Dit is om potentiële verstoring van de rapportage tijdens de kritieke periode aan het einde van het jaar te voorkomen. Zoals hieronder vermeld, zal de versie van het besturingssysteem vanaf oktober worden bevroren, maar vanwege de geleidelijke implementatie en het feit dat de meeste gebruikersagents worden bevroren naar de juiste versie van het besturingssysteem, schatten we dat dit gevolgen zal hebben voor &lt;3% van de Chrome Visitors.

>[!NOTE]
>
>Vanaf oktober 2022 starten nieuwe versies van Chromium-browsers de versie van het besturingssysteem die wordt weergegeven in de tekenreeks User-Agent, &#39;bevriezen&#39;. De versie van het besturingssysteem is een hoge entropiegelfunctie. Om de nauwkeurigheid van de versie van het besturingssysteem in uw rapportage te behouden, is het nodig dat u de verzamelingsbibliotheek configureert om deze hoge entropietpunten te verzamelen. In de loop van de tijd zal andere apparateninformatie van gebruiker-Agent worden bevroren, die cliëntwenken vereist om apparaat te handhaven rapporteert nauwkeurigheid.

>[!NOTE]
>
>AAM vereist dat er hoge entropiegels worden verzameld om de volledige functionaliteit te behouden. Als u [server-kant door:sturen aan AAM](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) dan kunt u inzameling van hoge entropiewenken willen toelaten.

## Veelgestelde vragen

+++**Waar kan ik meer over cliëntwenken leren?**

Dit [Google-blogbericht](https://web.dev/user-agent-client-hints/) is een goede referentie en een goed uitgangspunt.

+++

+++**Hoe laat ik de inzameling van cliëntwenken toe?**

Tips voor lage entropie worden automatisch door de browser opgegeven en worden opgenomen om apparaat- en browserinformatie af te leiden. De nieuwere versies van Web SDK (die met 2.12.0 beginnen) en AppMeasurement (die met 2.23.0 begint) kunnen worden gevormd om hoge entropiewenken via hun respectieve uitbreidingen van Markeringen of direct via een configuratieoptie te verzamelen. Zie aanwijzingen voor [Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/fundamentals/user-agent-client-hints.html?lang=en#enabling-high-entropy-client-hints) en [AppMeaurement](https://experienceleague.adobe.com/docs/analytics/implementation/vars/config-vars/collecthighentropyuseragenthints.html?lang=en).

Voor beide bibliotheken is het verzamelen van hoge entropiehints **standaard uitgeschakeld**.

+++

+++**Kan ik kiezen welke hoge entropips ik verzamel?**

Op dit moment niet. U kunt ervoor kiezen alle hints met hoge entropie of geen hints te verzamelen.

+++

+++**Wat zijn de verschillende waarden van de cliëntwenken?**

In de onderstaande tabel worden de tips voor cliënten vanaf oktober 2022 beschreven.

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

+++**Worden er wijzigingen aangebracht in apparaatrapportage in Analytics?**

De beschikbare apparaatvelden voor rapportage blijven ongewijzigd. De gegevens die voor die velden worden vastgelegd, kunnen veranderen afhankelijk van welk veld en hoe u verzameling voor clienttips hebt geconfigureerd.

+++

+++**Welke Analytics rapporterend gebieden worden afgeleid uit gebruiker-Agent?**

Deze gebieden worden direct afgeleid uit gebruiker-Agent maar user-Agent kan worden gebruikt om waarden voor andere apparaat verwante gebieden af te leiden, afhankelijk van de apparatendetails.

* [Browser](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser.html?lang=en)
* [Browsertype](https://experienceleague.adobe.com/docs/analytics/components/dimensions/browser-type.html?lang=en)
* [Besturingssysteem](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-systems.html?lang=en)
* [Typen besturingssystemen](https://experienceleague.adobe.com/docs/analytics/components/dimensions/operating-system-types.html?lang=en)
* [Mobiel apparaat en type mobiel apparaat](https://experienceleague.adobe.com/docs/analytics/components/dimensions/mobile-dimensions.html?lang=en)

+++

+++**Welke gedeelten van de user-Agent worden &quot;bevroren&quot;en wanneer?**

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html). Dit kan worden gewijzigd.

+++

+++**Welke analytische rapporteringsgebieden worden afgeleid van waarden die in hoge entropiewenken worden opgeslagen?**

Dit zal in tijd veranderen aangezien Google meer delen van de Gebruikersagent &quot;bevriest&quot;. Het eerste veld dat rechtstreeks moet worden beïnvloed, is &quot;Besturingssysteem&quot;, dat de versie van het besturingssysteem bevat Volgens de gepubliceerde tijdlijn van Google voor &quot;bevriezen&quot; van gebruikers-agent-tips, wordt de versie van het besturingssysteem vanaf eind oktober 2022 bevroren met Chromium versie 107. Op dat moment is de versie van het besturingssysteem in de gebruikersagent in sommige gevallen niet correct.

Zie de [tijdlijn gepubliceerd door Google](https://blog.chromium.org/2021/09/user-agent-reduction-origin-trial-and-dates.html) om de timing voor het bevriezen van andere gedeelten van user-Agent te zien.

+++

+++**Hoe zal Adobe cliëntwenken gebruiken om apparateninformatie af te leiden?**

Adobe gebruikt een derde, de Atlas van het Apparaat, die zowel de cliëntwenken als gebruiker-Agent zal gebruiken om apparateninformatie af te leiden.

+++

+++**Welke browsers worden beïnvloed door cliëntwenken?**

Clienttips zijn alleen van toepassing op chroombrowsers zoals Google Chrome en Microsoft Edge. Er is geen wijziging in de gegevens van andere browsers of mobiele apps.

+++

+++**Worden de cliëntwenken gesteund over onveilige verbindingen?**

Nee. Clienttips kunnen alleen worden verzameld via een beveiligde HTTP-verbinding, zoals HTTPS.

+++

+++**Hoe kan ik gegevens voor clienttips opnemen wanneer ik API-verzending gebruik?**

Zie documentatie voor het opnemen van deze via [API voor het invoegen van bulkgegevens](https://developer.adobe.com/analytics-apis/docs/2.0/guides/endpoints/bulk-data-insertion/file-format/).

+++

+++**Zijn de cliëntwenken beschikbaar in gegevens die naar AEP en CJA via de Bron van de Adobe schakelaar worden verzonden?**

Adobe is van plan om cliëntwenken in gegevens via de Schakelaar van de Bron van de Adobe in de eerste helft van 2023 te omvatten.

+++

+++**Hoe worden cliëntwenken vertegenwoordigd in XDM?**

Zie de [schemadocumentatie](https://github.com/adobe/xdm/blob/master/components/datatypes/browserdetails.schema.json#L121) in Adobe Experience Platform.

+++

+++**Zal AAM server-kant het door:sturen klantenwenken steunen?**

Ja. Clienttips worden opgenomen in de gegevens die naar AAM worden doorgestuurd. AAM vereist dat hips met hoge entropiegels worden verzameld om de volledige functionaliteit te behouden. Als u [server-kant door:sturen aan AAM](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) dan kunt u inzameling van high-entropy wenken willen toelaten.

+++

