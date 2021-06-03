---
title: Gegevensbronnen van transactie-id
description: Leer de algemene workflow voor het gebruik van gegevensbronnen voor transactie-id's.
exl-id: 5f26b15c-8d9c-46d5-860f-13fdfa21af2e
source-git-commit: 1ee6a1e69a277f0d3c0ffd1defca0d4cb098cc6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Gegevensbronnen van transactie-id

Met de gegevensbronnen van de transactie-id kunt u niet alleen online en offline gegevens naast elkaar weergeven, maar de gegevens aan elkaar koppelen. Het vereist het gebruik van de [`transactionID`](/help/implement/vars/page-vars/transactionid.md) variabele in uw implementatie Analytics.

Wanneer u een online treffer verzendt die een `transactionID` waarde bevat, neemt Adobe een &quot;momentopname&quot;van alle die variabelen op dat ogenblik worden geplaatst of voortgeduurd. Als een overeenkomende transactie-id wordt gevonden die via gegevensbronnen is geüpload, worden de offline- en onlinegegevens aan elkaar gekoppeld. Het maakt niet uit welke gegevensbron het eerst wordt gezien.

## Algemene workflow van gegevensbronnen voor transactie-id

Gebruik de volgende algemene workflow om te beginnen met het gebruik van gegevensbronnen voor Transactie-id:

1. Maak een gegevensbron (categorie Algemeen en type Algemene gegevensbron (transactie-id)).
1. Volg de installatiewizard voor de gegevensbron om een FTP-locatie op te halen waar u gegevens kunt uploaden en een sjabloonbestand voor gegevensbronnen kunt downloaden.
1. Werk uw implementatie bij om de `transactionID` variabele te omvatten.
1. Upload een gegevensbronbestand naar de FTP-site met een bestand `.fin`.

## Voorbeeld uploadbestand en implementatiecode

Als u het volgende bestand met gegevensbronnen hebt geüpload en de volgende code op uw site hebt geïmplementeerd, worden gegevens weergegeven die zijn gekoppeld aan rapportage. Het gegevensbrondossier gebruikt eVar1 en event1, terwijl de online implementatie eVar2 en event2 gebruikt. Aangezien de transactieidentiteitskaart aanpast, kon u gebeurtenis2 gegevens voor eVar1, en gebeurtenis1 gegevens voor eVar2 zien.

### Voorbeeldbestand

Download de sjabloon, werk de waarden bij en upload deze naar de FTP-locatie van de gegevensbronnen:

| `#` | `Example eVar1 name` | `Example event 1 name` | `1` |
|---|---|---|---|
| `Date` | `Evar 1` | `Event 1` | `transactionID` |
| `01/01/2020/12/00/00` | `Example eVar1 value` | `1` | `1234` |

### Voorbeeld-implementatiecode

Zie [`transactionID`](/help/implement/vars/page-vars/transactionid.md) in de gebruikershandleiding Implementeren voor een meer gedetailleerde uitleg van de transactie-id.

```js
var s = s_gi("examplersid");
s.eVar2 = "Example eVar2 value";
s.events = "event2";
s.transactionID = "1234";
s.t();
```
