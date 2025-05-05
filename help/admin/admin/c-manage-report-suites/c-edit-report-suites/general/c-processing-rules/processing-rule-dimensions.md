---
description: De beschikbare afmetingen en metriek die u kunt lezen en schrijven gebruikend verwerkingsregels.
subtopic: Processing rules
title: Beschikbare afmetingen voor verwerkingsregels
feature: Processing Rules
role: Admin
exl-id: ffd7a1d6-2c9d-41e7-9c75-9e47b6f9c283
source-git-commit: b53ef727adc563e05403c50d80bbd0c48bb8a054
workflow-type: tm+mt
source-wordcount: '712'
ht-degree: 1%

---

# Afmetingen en metingen beschikbaar voor verwerkingsregels

De beschikbare afmetingen en metriek die u kunt lezen en schrijven gebruikend verwerkingsregels.

## Aangepaste waarden en contextgegevens

| Waarde | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| Aangepaste waarde | Alleen-lezen | Aangepaste tekst of waarden die rechtstreeks in een verwerkingsregel worden getypt. |
| Samengevoegde waarde | Alleen-lezen | Waarden die worden gemaakt door twee waarden te combineren. U kunt bijvoorbeeld kanaal- en paginanaam combineren om een subcategorie te maken. |

## Aanraakkenmerken

| Kenmerk | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| Pagina-URL | Lezen + schrijven | De [ pagina URL ](/help/components/dimensions/page-url.md) afmeting. Het volgen van de verbinding overtreft deze dimensie alvorens verwerkingsregels te bereiken. Als u een pagina URL waarde gebruikend verwerkingsregels opnieuw opneemt, wordt de klap beschouwd als a [ mening van de Pagina ](/help/components/metrics/page-views.md) in plaats van de gebeurtenis van de a [ Pagina ](/help/components/metrics/page-events.md). Adobe raadt u aan te controleren op een waarde in de paginadimensie voordat u deze wijzigt. |
| Paginanaam | Lezen + schrijven | De [ dimensie van de Pagina ](/help/components/dimensions/page.md). Het volgen van de verbinding overtreft deze dimensie alvorens verwerkingsregels te bereiken. Als u een paginawaarde opnieuw opneemt gebruikend verwerkingsregels, wordt de klap beschouwd als a [ mening van de Pagina ](/help/components/metrics/page-views.md) in plaats van de gebeurtenis van de a [ Pagina ](/help/components/metrics/page-events.md). Adobe raadt u aan te controleren op een waarde in de paginadimensie voordat u deze wijzigt. |
| Reeks-id rapporteren | Alleen-lezen | De rapportsuite waarop de verwerkingsregel wordt uitgevoerd. Deze rapportsuite kan anders zijn dan de rapportsuite die oorspronkelijk via AppMeasurement is verzonden, bijvoorbeeld bij het gebruik van de VISTA-regels. |
| AppMeasurement-codeversie | Alleen-lezen | De AppMeasurement-bibliotheekversie die wordt gebruikt om de afbeeldingsaanvraag te genereren. |
| IP-adres | Alleen-lezen | Het IP-adres van de bezoeker. |
| Gebruikersagent | Alleen-lezen | De gebruikersagent van de bezoeker. |
| Referenter | Alleen-lezen | De [ dimensie van de Verwijzer ](/help/components/dimensions/referrer.md). |
| Tekenreeksparameter van query | Alleen-lezen | De waarde van een opgegeven parameter voor een querytekenreeks in de huidige URL. |
| Verwijzen naar parameter querytekenreeks | Alleen-lezen | De waarde van een opgegeven parameter voor een querytekenreeks in de verwijzende URL of een lege tekenreeks als er geen bestaat. |
| Verwijzen naar domein | Alleen-lezen | Het paginadomein van de verwijzende URL, inclusief subdomeinen. |
| Verwijzen naar hoofddomein | Alleen-lezen | Het paginadomein van de verwijzende URL, met uitzondering van subdomeinen. |
| Tekenreeks voor paginaquery | Alleen-lezen | Alle parameters van het vraagkoord en hun waarden in huidige URL. |
| Verwijzen naar queryreeks | Alleen-lezen | Alle parameters van het vraagkoord en hun waarden in verwijzende URL. |
| Paginapad | Alleen-lezen | Het paginapad van de huidige URL. Paginapad bevat geen parameters voor protocol-, domein- of queryreeksen. |
| Paginadomein | Alleen-lezen | Het paginadomein van de huidige URL, inclusief subdomeinen. Paginadomein bevat geen parameters voor paginapad of queryreeks. |
| Hoofddomein van pagina | Alleen-lezen | Het paginadomein van de huidige URL, exclusief subdomeinen. |
| Klantperspectief | Lezen + schrijven | Een markering die bepaalt of de treffer een mobiele achtergrondhit is. |

## Conversievariabelen

| Variabele | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| eVar 1-250 | Lezen + schrijven | [ eVar ](/help/components/dimensions/evar.md) afmetingen. |
| Campaign | Lezen + schrijven | De [ het Volgen code ](/help/components/dimensions/tracking-code.md) dimensie. |
| Aankoop-id | Lezen + schrijven | De implementatievariabele [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) . |
| Staat | Lezen + schrijven | De implementatievariabele [`state`](/help/implement/vars/page-vars/state.md) wordt uitgeschakeld. |
| Postcode | Lezen + schrijven | De [ dimensie van het Postcode ](/help/components/dimensions/zip-code.md). |
| Valutacode | Lezen + schrijven | De implementatievariabele [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) . BELANGRIJK: als u deze variabele op een ongeldige waarde instelt, wordt de hit genegeerd. |
| Transactie-id | Lezen + schrijven | De implementatievariabele [`transactionID`](/help/import/data-sources/transactionid.md) . |

>[!NOTE]
>Adobe biedt geen ondersteuning voor het instellen van de implementatievariabele [`products`](/help/implement/vars/page-vars/products.md) met behulp van verwerkingsregels.

## verkeersvariabelen

| Variabele | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| Prop 1-75 | Lezen + schrijven | [&#128279;](/help/components/dimensions/prop.md) afmetingen van 0&rbrace; Prop &lbrace;. |
| Hiërarchie 1-5 | Lezen + schrijven | [&#128279;](/help/components/dimensions/hierarchy.md) dimensies van 0&rbrace; Hiërarchie &lbrace;. |
| Server | Lezen + schrijven | De [ dimensie van de Server ](/help/components/dimensions/server.md). |
| Kanaal | Lezen + schrijven | De [ sectie van de Plaats ](/help/components/dimensions/site-section.md) dimensie. |

## Contextvariabelen

Alle [ variabelen van de Contextgegevens ](/help/implement/vars/page-vars/contextdata.md) die deze rapportreeks in vorige beeldverzoeken heeft gezien. Als de verwerkingsregels contextgegevens niet in een andere variabele plaatsen, worden die gegevens permanent verloren. Zie [ exemplaar een variabele van contextgegevens aan een eVar ](processing-rules-examples/processing-rules-copy-context-data.md) en [ plaats een gebeurtenis gebruikend een variabele van contextgegevens ](processing-rules-examples/processing-rules-copy-context-data-event.md) voor gebruiksvoorbeelden.

## Gebeurtenissen met succes

Met verwerkingsregels kunnen gebeurtenissen worden ingesteld, maar deze kunnen niet als voorwaarden worden gelezen. Stel de vervolgkeuzelijst voor regelactie in op **[!UICONTROL Set event]** om de beschikbare metriek te zien op verhogen.

| Variabele | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| Orders | Alleen schrijven | De [ orden ](/help/components/metrics/orders.md) metrisch. |
| Houtskaarten | Alleen schrijven | De [ metrische Havens ](/help/components/metrics/carts.md). |
| Winkelweergaven | Alleen schrijven | De [ metrische meningen van het Kart ](/help/components/metrics/cart-views.md). |
| Afbeeldingen | Alleen schrijven | De [ metrische controles ](/help/components/metrics/checkouts.md). |
| Extra winkelwagentjes | Alleen schrijven | De [ metrische toevoegingen van de Kar ](/help/components/metrics/cart-additions.md). |
| Winkelwagentjes | Alleen schrijven | De [ verwijdering van de Kar ](/help/components/metrics/cart-removals.md) metrisch. |
| Gebeurtenis 1-1000 | Alleen schrijven | [ de gebeurtenissen van de Douane ](/help/components/metrics/custom-events.md). |
| Productweergaven | Alleen schrijven | De [ metrische meningen van het Product ](/help/components/metrics/product-views.md). |

