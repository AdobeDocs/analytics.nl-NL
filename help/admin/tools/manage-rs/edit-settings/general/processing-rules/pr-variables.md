---
description: De beschikbare afmetingen en metriek die u kunt lezen en schrijven gebruikend verwerkingsregels.
subtopic: Processing rules
title: Afmetingen en metingen beschikbaar voor verwerkingsregels
feature: Processing Rules
role: Admin
exl-id: ffd7a1d6-2c9d-41e7-9c75-9e47b6f9c283
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 2%

---

# Afmetingen en metingen beschikbaar voor verwerkingsregels

De beschikbare afmetingen en metriek die u kunt lezen en schrijven gebruikend verwerkingsregels.

## Aangepaste waarden en contextgegevens

| Waarde | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| **de waarde van de Douane** | Alleen-lezen | Aangepaste tekst of waarden die rechtstreeks in een verwerkingsregel worden getypt. |
| **Samengevoegde waarde** | Alleen-lezen | Waarden die worden gemaakt door twee waarden te combineren. U kunt bijvoorbeeld kanaal- en paginanaam combineren om een subcategorie te maken. |

## Aanraakkenmerken

| Kenmerk | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| **pagina URL** | Lezen + schrijven | De [&#x200B; pagina URL &#x200B;](/help/components/dimensions/page-url.md) afmeting. Het volgen van de verbinding overtreft deze dimensie alvorens verwerkingsregels te bereiken. Als u een pagina URL waarde gebruikend verwerkingsregels opnieuw opneemt, wordt de klap beschouwd als a [&#x200B; mening van de Pagina &#x200B;](/help/components/metrics/page-views.md) in plaats van de gebeurtenis van de a [&#x200B; Pagina &#x200B;](/help/components/metrics/page-events.md). Adobe raadt u aan te controleren op een waarde in de paginadimensie voordat u deze wijzigt. |
| **de naam van de Pagina** | Lezen + schrijven | De [&#x200B; dimensie van de Pagina &#x200B;](/help/components/dimensions/page.md). Het volgen van de verbinding overtreft deze dimensie alvorens verwerkingsregels te bereiken. Als u een paginawaarde opnieuw opneemt gebruikend verwerkingsregels, wordt de klap beschouwd als a [&#x200B; mening van de Pagina &#x200B;](/help/components/metrics/page-views.md) in plaats van de gebeurtenis van de a [&#x200B; Pagina &#x200B;](/help/components/metrics/page-events.md). Adobe raadt u aan te controleren op een waarde in de paginadimensie voordat u deze wijzigt. |
| **ReeksIdentiteitskaart van het Rapport** | Alleen-lezen | De rapportsuite waarop de verwerkingsregel wordt uitgevoerd. Deze rapportsuite kan anders zijn dan de rapportsuite die oorspronkelijk via AppMeasurement is verzonden, bijvoorbeeld bij het gebruik van de VISTA-regels. |
| **de codeversie van AppMeasurement** | Alleen-lezen | De AppMeasurement-bibliotheekversie die wordt gebruikt om de afbeeldingsaanvraag te genereren. |
| **IP adres** | Alleen-lezen | Het IP-adres van de bezoeker. |
| **de agent van de Gebruiker** | Alleen-lezen | De gebruikersagent van de bezoeker. |
| **Referrer** | Alleen-lezen | De [&#x200B; dimensie van de Verwijzer &#x200B;](/help/components/dimensions/referrer.md). |
| **het koordparameter van de Vraag** | Alleen-lezen | De waarde van een opgegeven parameter voor een querytekenreeks in de huidige URL. |
| **Verwijzend de parameter van het vraagkoord** | Alleen-lezen | De waarde van een opgegeven parameter voor een querytekenreeks in de verwijzende URL of een lege tekenreeks als er geen bestaat. |
| **Verwijzend domein** | Alleen-lezen | Het paginadomein van de verwijzende URL, inclusief subdomeinen. |
| **Verwijzend worteldomein** | Alleen-lezen | Het paginadomein van de verwijzende URL, met uitzondering van subdomeinen. |
| **koord van de de vraagvraag van de Pagina** | Alleen-lezen | Alle parameters van het vraagkoord en hun waarden in huidige URL. |
| **Verwijzend vraagkoord** | Alleen-lezen | Alle parameters van het vraagkoord en hun waarden in verwijzende URL. |
| **Pad van de Pagina** | Alleen-lezen | Het paginapad van de huidige URL. Paginapad bevat geen parameters voor protocol-, domein- of queryreeksen. |
| **domein van de Pagina** | Alleen-lezen | Het paginadomein van de huidige URL, inclusief subdomeinen. Paginadomein bevat geen parameters voor paginapad of queryreeks. |
| **het worteldomein van de Pagina** | Alleen-lezen | Het paginadomein van de huidige URL, exclusief subdomeinen. |
| **het perspectief van de Klant** | Lezen + schrijven | Een markering die bepaalt of de treffer een mobiele achtergrondhit is. |

## Conversievariabelen

| Variabele | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| **eVar 1-250** | Lezen + schrijven | [&#x200B; eVar &#x200B;](/help/components/dimensions/evar.md) afmetingen. |
| **Campaign** | Lezen + schrijven | De [&#x200B; het Volgen code &#x200B;](/help/components/dimensions/tracking-code.md) dimensie. |
| **identiteitskaart van de Aankoop** | Lezen + schrijven | De implementatievariabele [`purchaseID`](/help/implement/vars/page-vars/purchaseid.md) . |
| **Staat** | Lezen + schrijven | (In ruste) De implementatievariabele [`state`](/help/implement/vars/page-vars/state.md) . |
| **Postcode** | Lezen + schrijven | De [&#x200B; dimensie van het Postcode &#x200B;](/help/components/dimensions/zip-code.md). |
| **code van de Valuta** | Lezen + schrijven | De implementatievariabele [`currencyCode`](/help/implement/vars/config-vars/currencycode.md) . BELANGRIJK: als u deze variabele op een ongeldige waarde instelt, wordt de hit genegeerd. |
| **Transactie-id** | Lezen + schrijven | De implementatievariabele [`transactionID`](/help/import/data-sources/transactionid.md) . |

>[!NOTE]
>Adobe biedt geen ondersteuning voor het instellen van de implementatievariabele [`products`](/help/implement/vars/page-vars/products.md) met behulp van verwerkingsregels.

## verkeersvariabelen

| Variabele | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| **Prop 1-75** | Lezen + schrijven | [&#x200B; afmetingen van 0&rbrace; Prop &lbrace;.](/help/components/dimensions/prop.md) |
| **Hiërarchie 1-5** | Lezen + schrijven | (In ruste) [&#x200B; Hiërarchie &#x200B;](/help/components/dimensions/hierarchy.md) dimensies. |
| **Server** | Lezen + schrijven | De [&#x200B; dimensie van de Server &#x200B;](/help/components/dimensions/server.md). |
| **Kanaal** | Lezen + schrijven | De [&#x200B; sectie van de Plaats &#x200B;](/help/components/dimensions/site-section.md) dimensie. |

## Contextvariabelen

Alle [&#x200B; variabelen van de Contextgegevens &#x200B;](/help/implement/vars/page-vars/contextdata.md) die deze rapportreeks in de laatste 30 dagen heeft gezien. Zie [&#x200B; het gebruiksgevallen van de Regels van de Verwerking &#x200B;](pr-use-cases.md) voor gebruiksvoorbeelden.

>[!IMPORTANT]
>
>Als de verwerkingsregels een bepaalde variabele van contextgegevens aan een andere variabele (zoals een steun of eVar) niet in kaart brengen, wordt de waarde in de variabele van contextgegevens permanent verloren.

## Gebeurtenissen met succes

Met verwerkingsregels kunnen gebeurtenissen worden ingesteld, maar deze kunnen niet als voorwaarden worden gelezen. Stel de vervolgkeuzelijst voor regelactie in op **[!UICONTROL Set event]** om de beschikbare metriek te zien op verhogen.

| Variabele | Status lezen/schrijven | Beschrijving |
| --- | --- | --- |
| **Orders** | Alleen schrijven | De [&#x200B; orden &#x200B;](/help/components/metrics/orders.md) metrisch. |
| **Houtskaarten** | Alleen schrijven | De [&#x200B; metrische Havens &#x200B;](/help/components/metrics/carts.md). |
| {de meningen van 0} Kaart **&#x200B;**&#x200B;| Alleen schrijven | De [&#x200B; metrische meningen van het Kart &#x200B;](/help/components/metrics/cart-views.md). |
| **Betalingen** | Alleen schrijven | De [&#x200B; metrische controles &#x200B;](/help/components/metrics/checkouts.md). |
| **toevoegingen van de Kaart** | Alleen schrijven | De [&#x200B; metrische toevoegingen van de Kar &#x200B;](/help/components/metrics/cart-additions.md). |
| **de verwijderingen van de Kar** | Alleen schrijven | De [&#x200B; verwijdering van de Kar &#x200B;](/help/components/metrics/cart-removals.md) metrisch. |
| **Gebeurtenis 1-1000** | Alleen schrijven | [&#x200B; de gebeurtenissen van de Douane &#x200B;](/help/components/metrics/custom-events.md). |
| **de meningen van het Product** | Alleen schrijven | De [&#x200B; metrische meningen van het Product &#x200B;](/help/components/metrics/product-views.md). |
