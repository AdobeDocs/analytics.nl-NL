---
title: Overzicht van dynamische accounts
description: Leer de workflow voor het dynamisch selecteren van een rapportsuite met H Code.
translation-type: tm+mt
source-git-commit: f313fd0c9ffda054a18ad1d457a74602b08e51fa

---


# Overzicht van dynamische accounts

> [!IMPORTANT] Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of Adobe Experience Platform Launch.

Dynamische accounts zijn een implementatiefunctie waarmee u kunt bepalen welke rapportsuite moet worden gebruikt op basis van criteria die u definieert. Als uw organisatie meer dan één rapportreeks maar de zelfde implementatie tussen uw plaatsen vereist, is de dynamische rekeningen een goede oplossing.

> [!TIP] Adobe raadt u aan gegevens naar één rapportsuite te verzenden en deze vervolgens zo nodig met virtuele rapportsuites te scheiden. Zie [Globale rapportenreeks overwegingen](../../../prepare/global-rs.md) voor meer informatie.

3 variabelen worden gebruikt om een rapportreeks dynamisch te selecteren.

* [`dynamicAccountSelection`](dynamicaccountselection.md): Dynamische accountselectie in- of uitschakelen.
* [`dynamicAccountMatch`](dynamicaccountmatch.md): Hiermee bepaalt u welke waarde u wilt observeren. Bijvoorbeeld de URL of een queryreeks.
* [`dynamicAccountList`](dynamicaccountlist.md): Vergelijkt de waarden met `dynamicAccountMatch`, en als een gelijke wordt gevonden, bevolkt de `account` variabele.

Als `dynamicAccountSelection = true`, wordt de waarde binnen `dynamicAccountMatch` vergeleken met `dynamicAccountList`. Als de waarden in `dynamicAccountList` gelijke zijn, is identiteitskaart van de rapportreeks inbegrepen in de `account` variabele.

## Standaardrapportsuite

De `account` variabele kan eerst worden ingesteld en fungeert als standaardwaarde voor het geval een van de opgegeven tekenreeksen niet kan worden gevonden. Bijvoorbeeld:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

Als `location.hostname` dit niet het geval was `dev.example.com` of `example.com`, wordt de hit naar `examplersiddefault`.

## Tags toevoegen met meerdere suite

Tags met meerdere suite kunnen worden gebruikt bij het selecteren van dynamische accounts. Bijvoorbeeld:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

Als `location.hostname` bevat `example.com`, wordt de treffer verzonden naar zowel `examplersid1` als `examplersid2`.
