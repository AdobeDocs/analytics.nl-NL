---
title: Overzicht van dynamische accounts
description: Leer de workflow voor het dynamisch selecteren van een rapportsuite met H Code.
feature: Implementation Basics
exl-id: 6f35dd71-29ad-4923-b1f7-9c7d6ca45bd8
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 1%

---

# Overzicht van dynamische accounts

>[!IMPORTANT]
>
>Dynamische accounts worden alleen ondersteund met behulp van verouderde JavaScript-implementaties (H Code). Deze variabelen worden niet ondersteund in huidige AppMeasurementen bibliotheken of tags in Adobe Experience Platform.

Dynamische accounts zijn een implementatiefunctie waarmee u kunt bepalen welke rapportsuite moet worden gebruikt op basis van criteria die u definieert. Als uw organisatie meer dan één rapportreeks maar de zelfde implementatie tussen uw plaatsen vereist, is de dynamische rekeningen een goede oplossing.

>[!TIP]
>
>Adobe raadt aan gegevens naar één rapportsuite te verzenden en deze vervolgens zo nodig met virtuele rapportsuites te scheiden. Zie [Overwegingen voor algemene rapporten](../../../prepare/global-rs.md) voor meer informatie .

3 variabelen worden gebruikt om een rapportreeks dynamisch te selecteren.

* [`dynamicAccountSelection`](dynamicaccountselection.md): Dynamische accountselectie in- of uitschakelen.
* [`dynamicAccountMatch`](dynamicaccountmatch.md): bepaalt welke waarde moet worden waargenomen. Bijvoorbeeld de URL of een queryreeks.
* [`dynamicAccountList`](dynamicaccountlist.md): vergelijkt de waarden met `dynamicAccountMatch`, en als een gelijke wordt gevonden, bevolkt `account` variabele.

Indien `dynamicAccountSelection = true`, de waarde binnen `dynamicAccountMatch` wordt vergeleken met `dynamicAccountList`. Als de waarden in `dynamicAccountList` match, de rapportsuite-id is opgenomen in de `account` variabele.

## Standaardrapportsuite

De `account` De variabele kan eerst worden ingesteld en fungeert als standaardwaarde voor het geval een van de opgegeven tekenreeksen niet kan worden gevonden. Bijvoorbeeld:

```javascript
s_account = "examplersiddefault";
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersiddev=dev.example.com;examplersidprod=example.com";
```

Indien `location.hostname` was geen `dev.example.com` of `example.com`, wordt de treffer naar `examplersiddefault`.

## Tags toevoegen met meerdere suite

Tags met meerdere suite kunnen worden gebruikt bij het selecteren van dynamische accounts. Bijvoorbeeld:

```js
s.dynamicAccountSelection = true;
s.dynamicAccountMatch = location.hostname;
s.dynamicAccountList="examplersid1,examplersid2=example.com";
```

Indien `location.hostname` contains `example.com`, wordt de treffer naar beide verzonden `examplersid1` en `examplersid2`.
