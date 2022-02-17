---
title: Gegevensbronnen van transactie-id
description: Leer de algemene workflow voor het gebruik van gegevensbronnen voor transactie-id's.
feature: Data Sources
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 0%

---

# Gegevensbronnen van transactie-id

Met de gegevensbronnen van de transactie-id kunt u niet alleen online en offline gegevens naast elkaar weergeven, maar de gegevens aan elkaar koppelen. Het vereist het gebruik van [`transactionID`](/help/implement/vars/page-vars/transactionid.md) in uw analytische implementatie.

Wanneer u een online hit verzendt die een `transactionID` waarde, neemt Adobe een &quot;momentopname&quot;van alle variabelen die op dat ogenblik worden geplaatst of voortgeduurd. Als een overeenkomende transactie-id wordt gevonden die via gegevensbronnen is geüpload, worden de offline- en onlinegegevens aan elkaar gekoppeld.

Als u transacties wilt gebruiken, moet de online hit met een transactie-id zijn verzonden naar en verwerkt voordat gegevens uit de transactiegegevens met die transactie-id zijn verzonden. De online hit bevat variabelen (eVars, enz.), maar geen gebeurtenissen, die zich op de online hit bevonden met de transactie-id-informatie bevonden.

Wanneer een hit met een transactiegegevensbron wordt verzonden, zoekt de transactie-id op de hit bij een gegevensbrontransactie de vars enz. op. (geen gebeurtenissen) die zijn gekoppeld aan de oorspronkelijke online hit met die transactie-id. Deze variabelen worden gebruikt bij een hit met een gegevensbrontransactie als er geen waarde was voor een variabele die wordt doorgegeven aan de hit met een gegevensbrontransactie.

## Voorbeeld

Als een online hit met transactie-id 1256 wordt doorgegeven en doorgegeven `evar1=blue`, `evar2=water` en `event1` worden ingesteld, vervolgens worden de transactiegegevens voor transactie-id 1256 niet opgeslagen met `evar1=blue`, `evar2=water`. Er worden geen gebeurteniswaarden opgeslagen als onderdeel van de transactiegegevens.

Nu veronderstellen dat een raakpunt van de gegevensbrontransactie dan door het systeem met transactie identiteitskaart 1256 wordt overgegaan en `evar1=yellow`, `evar3=mountain` en `event2` set. Het systeem vindt de opgeslagen transactiegegevens en in de reeksen van de gegevensbrontransactie `evar2=water` (omdat dit is wat op de originele hit werd geplaatst). Wordt niet ingesteld `evar1=blue` (zoals bij de oorspronkelijke hit) omdat er een waarde was voor `evar1` (geel) al ingesteld bij de hit van de gegevensbrontransactie.  Het resultaat van een hit bij een gegevensbrontransactie is dus `evar1=yellow`, `evar2=water` (van de originele online hit) en `evar3=mountain`. Deze 3 waarden hebben `event2` set - de gebeurtenis van de hit voor een gegevensbrontransactie.

Geen waarden van raakgebied gegevensbrontransactie `event1` Hiermee stelt u in wanneer de hit bij een gegevensbrontransactie wordt verwerkt.

## Algemene workflow van gegevensbronnen voor transactie-id

Gebruik de volgende algemene workflow om te beginnen met het gebruik van gegevensbronnen voor Transactie-id:

1. Maak een gegevensbron (categorie Algemeen en type Algemene gegevensbron (transactie-id)).
1. Volg de installatiewizard voor de gegevensbron om een FTP-locatie op te halen waar u gegevens kunt uploaden en een sjabloonbestand voor gegevensbronnen kunt downloaden.
1. Werk uw implementatie bij om de `transactionID` variabele.
1. Upload een gegevensbronbestand naar de FTP-site met een `.fin` bestand.

## Voorbeeld uploadbestand en implementatiecode

Als u het volgende bestand met gegevensbronnen hebt geüpload en de volgende code op uw site hebt geïmplementeerd, worden gegevens weergegeven die zijn gekoppeld aan rapportage. Het gegevensbrondossier gebruikt eVar1 en event1, terwijl de online implementatie eVar2 en event2 gebruikt. Aangezien de transactieidentiteitskaart aanpast, kon u gebeurtenis2 gegevens voor eVar1, en gebeurtenis1 gegevens voor eVar2 zien.

### Voorbeeldbestand

Download de sjabloon, werk de waarden bij en upload deze naar de FTP-locatie van de gegevensbronnen:

| `#` | `Example eVar1 name` | `Example event 1 name` | `1` |
|---|---|---|---|
| `Date` | `Evar 1` | `Event 1` | `transactionID` |
| `01/01/2020/12/00/00` | `Example eVar1 value` | `1` | `1234` |

### Voorbeeld-implementatiecode

Voor een gedetailleerdere uitleg over transactie-id raadpleegt u [`transactionID`](/help/implement/vars/page-vars/transactionid.md) In de de gebruikersgids van het Uitvoeren.

```js
var s = s_gi("examplersid");
s.eVar2 = "Example eVar2 value";
s.events = "event2";
s.transactionID = "1234";
s.t();
```
