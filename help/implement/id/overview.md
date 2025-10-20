---
title: Identificatie bezoeker in Adobe Analytics
description: Leer hoe u bezoekers in Adobe Analytics kunt identificeren aan de hand van de nieuwste tips en trucs.
source-git-commit: 779ba5b0a1d71467aaaf3872fd707cc323ae8af2
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Identificatie bezoeker in Adobe Analytics

De identificatie van de bezoeker is centraal aan de waarde die Adobe Analytics voor het begrip van online gebruikersgedrag verstrekt. Het impliceert het verbinden van klappen aan de zelfde persoon in tijd gebruikend een gemeenschappelijke herkenningsteken. Nauwkeurige identificatie van bezoekers zorgt voor betrouwbare meetwaarden en ondersteunt een gezonde implementatiestrategie. Adobe raadt organisaties aan om prioriteit te geven aan moderne identiteitsdiensten voor consistentie en gegevensintegriteit op verschillende platforms.

Bezoekersidentificatie in Adobe Analytics bestaat uit de volgende onderdelen:

* Id aan de clientzijde: Wordt meestal opgeslagen in een cookie van de eerste fabrikant. Implementaties die afhankelijk zijn van cookies van derden zijn minder consistent met de identificatie van bezoekers vanwege de moderne privacystandaarden voor browsers.
* Id aan de serverzijde: Elke bezoeker-id van Analytics is gekoppeld aan een profiel op Adobe-servers. Deze bezoekersprofielen zijn wat persistentie op variabelen zoals [&#x200B; eVars &#x200B;](/help/components/dimensions/evar.md) toestaat. Profielen worden na een inactiviteit van ten minste 13 maanden verwijderd, ongeacht het verlopen van de cookie van de bezoeker-id.

## Adobe Analytics-identificatievolgorde van vluchtuitvoeringen

Wanneer Adobe een treffer ontvangt, worden de volgende controles in volgorde uitgevoerd. Als een bepaalde eigenschap aanwezig is, gebruikt Adobe die id voor de hit. Als een hit meerdere id&#39;s bevat, wordt alleen de eerste methode gebruikt.

| Volgorde gebruikt | Query-parameter | Presenteren wanneer |
|---|---|---|
| **1 <sup> st</sup>** | `vid` | De variabele [`visitorID`](/help/implement/vars/config-vars/visitorid.md) wordt ingesteld. |
| **2 <sup> en</sup>** | `aid` | De bezoeker heeft een bestaand [`s_vi` &#x200B;](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) koekje. Plaats op implementaties zonder of voorafgaand aan het uitvoeren van de dienst van identiteitskaart van de Bezoeker. |
| **3 <sup> rd</sup>** | `mid` | De bezoeker heeft een bestaand [`s_ecid` &#x200B;](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) koekje. Plaats op implementaties gebruikend de [&#x200B; dienst van de Identiteit van Adobe Experience Cloud &#x200B;](https://experienceleague.adobe.com/docs/id-service/using/home.html). Adobe raadt aan de id-service waar mogelijk te gebruiken voor alle implementaties. |
| **4 <sup> de</sup>** | `fid` | De bezoeker heeft een bestaand [`s_fid` &#x200B;](https://experienceleague.adobe.com/en/docs/core-services/interface/data-collection/cookies/analytics) cookie, of als `aid` en `mid` om welke reden dan ook niet kunnen worden ingesteld. |
| **5 <sup> de</sup>** | IP Adres, de Agent van de Gebruiker, IP van de Gateway Adres | Wordt gebruikt als laatste redmiddel om een unieke bezoeker te identificeren als de browser van de bezoeker geen cookies accepteert. |

## Gedrag dat van invloed is op het aantal unieke bezoekers

Unieke bezoekersidentificatoren worden doorgaans opgeslagen in een browsercookie. Een nieuwe unieke bezoeker wordt geteld als een bezoeker een van de volgende handelingen uitvoert:

* Wist op elk gewenst moment hun cookies. Eén unieke bezoeker wordt meegeteld voor een hit nadat de cache is gewist.
* Cookies van bezoekersidentiteitskaart verlopen vanwege de privacyinstellingen van hun browser. Sommige browsers bevatten methoden voor het bijhouden van fouten die de levensduur van cookies beperken.
* Opent een andere browser op dezelfde computer. Eén unieke bezoeker wordt per browser geteld.
* Hiermee opent u een Private Browsing-sessie (zoals het tabblad Chrome Incognito). Eén unieke bezoeker wordt per bladersessie geteld nadat alle tabbladen zijn gesloten.
* Bezoekt uw site op verschillende apparaten. Eén unieke bezoeker wordt geteld per apparaat.
* Bezoek uw site na meer dan 13 maanden inactiviteit.

Overweeg het gebruiken van [&#x200B; Stitching &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/stitching/overview) in Customer Journey Analytics om de zelfde persoon te identificeren gebruikend veelvoudige browsers of veelvoudige apparaten.

## Gedrag dat geen invloed heeft op het aantal unieke bezoekers

Een nieuwe unieke bezoeker wordt *niet* geteld, zolang het bezoekersherkenningsteken wordt bewaard:

* Sluit hun browser (minder dan 13 maanden)
* Hiermee wordt de browser bijgewerkt naar de nieuwste versie
* Start de computer opnieuw op
