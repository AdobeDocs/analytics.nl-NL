---
title: Overzicht van dynamische accounts
description: Leer de workflow voor het dynamisch selecteren van een rapportsuite met H Code.
exl-id: 6f35dd71-29ad-4923-b1f7-9c7d6ca45bd8
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 4%

---

# Overzicht van dynamische accounts

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in de huidige AppMeasurement-bibliotheken of -tags in Adobe Experience Platform.

Dynamische accounts zijn een implementatiefunctie waarmee u kunt bepalen welke rapportsuite moet worden gebruikt op basis van criteria die u definieert. Als uw organisatie meer dan één rapportreeks maar de zelfde implementatie tussen uw plaatsen vereist, is de dynamische rekeningen een goede oplossing.

>[!TIP]
>
>Adobe raadt u aan gegevens naar één rapportsuite te verzenden en vervolgens indien nodig virtuele rapportsuites te gebruiken om gegevens te scheiden. Zie [Algemene overwegingen van de rapportreeks](../../../prepare/global-rs.md) voor meer informatie.

3 variabelen worden gebruikt om een rapportreeks dynamisch te selecteren.

* [`dynamicAccountSelection`](dynamicaccountselection.md): Dynamische accountselectie in- of uitschakelen.
* [`dynamicAccountMatch`](dynamicaccountmatch.md): Hiermee bepaalt u welke waarde u wilt observeren. Bijvoorbeeld de URL of een queryreeks.
* [`dynamicAccountList`](dynamicaccountlist.md): Vergelijkt de waarden met  `dynamicAccountMatch`, en als een gelijke wordt gevonden, bevolkt de  `account` variabele.

Als `dynamicAccountSelection = true`, wordt de waarde binnen `dynamicAccountMatch` vergeleken met `dynamicAccountList`. Als de waarden in `dynamicAccountList` aanpassen, is identiteitskaart van de rapportreeks inbegrepen in `account` variabele.

## Standaardrapportsuite

De variabele `account` kan als eerste worden ingesteld en fungeert als standaardwaarde voor het geval een van de opgegeven tekenreeksen niet kan worden gevonden. Bijvoorbeeld:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

Als `location.hostname` noch `dev.example.com` of `example.com` was, zou de hit worden verzonden naar `examplersiddefault`.

## Tags toevoegen met meerdere suite

Tags met meerdere suite kunnen worden gebruikt bij het selecteren van dynamische accounts. Bijvoorbeeld:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

Als `location.hostname` `example.com` bevat, wordt de hit verzonden naar zowel `examplersid1` als `examplersid2`.
