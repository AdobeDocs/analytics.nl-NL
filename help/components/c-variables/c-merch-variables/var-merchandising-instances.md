---
description: Beschrijft hoe de instanties op het merchandising variabelen worden geteld.
keywords: Analytics Implementation
title: Instanties van variabelen voor handelsdoeleinden
topic: Developer and implementation
uuid: 4cdfd53e-88aa-48cf-a135-98f7fc8dcece
translation-type: tm+mt
source-git-commit: ''

---


# Instanties van variabelen voor handelsdoeleinden

Beschrijft hoe de instanties op het merchandising variabelen worden geteld.

Instanties worden momenteel niet ondersteund voor variabelen die worden gedistribueerd. Als u instanties in een rapport opmerkt die een koopvaardijvariabele bevatten, wijst het erop dat eVar in sommige plaatsen buiten het productkoord wordt geplaatst en niet als ware telling van instanties voor de geselecteerde handelaardiserende variabele zou moeten worden beschouwd.

Als u de Syntaxis van de Variabele van de Omzetting gebruikt, wordt een instantie geteld telkens als de variabele wordt geplaatst. De instantie wordt echter aan &quot;Geen&quot; toegewezen, tenzij het volgende gebeurt telkens wanneer de variabele wordt ingesteld:

* Er wordt een bindingsgebeurtenis ingesteld.
* De productvariabele wordt ingesteld.
* De merchandising Var heeft een waarde.

De volgende instantie van eVar1 wordt bijvoorbeeld toegewezen aan &quot;Outdoor:Ski Goggles&quot;:

```js
s.eVar1="Outdoors:Ski Goggles" 
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

In het volgende voorbeeld wordt de instantie van eVar1 echter toegewezen aan &quot;Geen&quot; omdat niet aan alle voorwaarden wordt voldaan wanneer eVar wordt ingesteld (er is geen bindende gebeurtenis en de productvariabele is niet ingesteld):

Pagina 1 van het bezoek:

```js
s.eVar1="Outdoors:Ski Goggles"
```

Pagina 2 van het bezoek:

```js
s.events="prodView" 
s.products=";Fernie Snow Goggles"
```

De toewijzing aan &quot;niets&quot;komt voor als u een waarde voor een eVar op een pagina plaatst waar geen bindende gebeurtenis voorkomt, of als u de waarde van Var in het productkoord zonder een bindende gebeurtenis plaatst.

> [!NOTE] De huidige functionaliteit voor het tellen van instanties op handelswisselende variabelen wordt herzien en zal in een komende versie veranderen.

