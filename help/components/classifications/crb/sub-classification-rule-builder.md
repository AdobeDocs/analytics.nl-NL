---
description: U kunt de Classification Rule Builder niet combineren met subclassificaties.
title: Subclassificaties en de Rule Builder
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 2%

---


# Subclassificaties en de Rule Builder

U kunt de Bouwer van de Regel van de Classificatie met sub-classificaties combineren als u ervoor zorgt dat elke subclassificatie een ouderwaarde heeft.

Het combineren van de functie voor classificatieregel met subclassificaties kan het beheer van classificaties vereenvoudigen en het aantal vereiste regels verminderen. Dit kan handig zijn als uw code voor bijhouden bestaat uit codes die u afzonderlijk wilt classificeren.

Zie [Subclassificaties](/help/components/classifications/c-sub-classifications.md) voor conceptuele informatie over subclassificaties.

## Voorbeeld

Stel de volgende code in:

`channel:broad_campaign:creative`

Met een classificatiehiërarchie kunt u een classificatie toepassen op een classificatie (*`sub-classification`* genoemd). Dit betekent dat u de importer kunt gebruiken als een relationele database, met meerdere tabellen. In de ene tabel worden volledige volgcodes toegewezen aan sleutels en in de andere tabel worden deze codes toegewezen aan andere tabellen.

![](assets/sub_class_table.png)

Nadat u deze structuur op zijn plaats hebt, kunt u [Classifications Rule Builder](/help/components/classifications/crb/classification-rule-builder.md) gebruiken om kleine dossiers te uploaden die slechts de raadplegingslijsten (de groene en rode lijsten in het voorafgaande beeld) bijwerken. Dan, kunt u de regelbouwer gebruiken om de belangrijkste classificatielijst bijgewerkt te houden.

De volgende taak beschrijft hoe te om dit te verwezenlijken.

## Subclassificaties instellen met de Rule Builder{#task_2D9016D8B4E84DBDAF88555E5369546F}

De stappen van het voorbeeld die beschrijven hoe u sub-classificaties kunt uploaden gebruikend de Bouwer van de Regel.

>[!NOTE]
>
>Deze stappen beschrijven hoe te om het gebruiksgeval te verwezenlijken dat in [Subclassificaties en de Bouwer van de Regel wordt beschreven](/help/components/classifications/crb/sub-classification-rule-builder.md).

1. Creëer classificaties en subclassificaties in [Classification Manager](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html).

   Voorbeeld:

   ![Stapinfo](assets/sub_class_create.png)

1. In [de Bouwer van de Regel van classificaties](/help/components/classifications/crb/classification-rule-builder.md), classificeer de sub-classificatiesleutel van de originele het volgen code.

   U voert dit uit gebruikend een regelmatige uitdrukking. In dit voorbeeld zou de regel voor het vullen *`Broad Campaign code`* deze reguliere expressie gebruiken:

   | `#` | Type regel | Overeenkomst | Classificatie instellen | Naar |
   |---|---|---|---|---|
   |  | Gewone uitdrukking | `[^\:]:([^\:]):([^\:]`) | Code brede campagne | `$1` |
   |  | Gewone uitdrukking | `[^\:]:([^\:]):([^\:]`) | Creatieve code | `$2` |

   >[!NOTE]
   >
   >Op dit punt, bevolkt u niet de sub-classificaties *`Campaign Type`* en *`Campaign Director`*.

1. Upload een classificatiebestand dat alleen de opgegeven subclassificaties bevat.

   Zie [Classificaties op meerdere niveaus](/help/components/classifications/c-sub-classifications.md).

   Voorbeeld:

   | Sleutel | Kanaal | Code brede campagne | Code&amp;amp voor uitgebreide campagne;Hoed;Type campagne | Code&amp;amp voor uitgebreide campagne;Hoed;Campagne voor Director | ... |
   |---|---|---|---|---|---|
   | * |  | 111 | Merk | Suzanne |  |
   | * |  | 222 | Merk | Frank |  |

1. Upload een klein bestand (zoals hierboven weergegeven) om de opzoektabellen te onderhouden.

   U zou dit dossier, bijvoorbeeld, uploaden wanneer nieuw *`Broad Campaign code`* wordt geïntroduceerd. Dit bestand is van toepassing op eerder geclassificeerde waarden. En als u een nieuwe subclassificatie maakt (zoals *`Creative Theme`* als een subclassificatie van *`Creative code`*), uploadt u alleen het bestand voor de subclassificatie in plaats van het volledige classificatiebestand.

   Voor de rapportage van deze subclassificaties werken deze precies op de bovenste classificaties. Dit vermindert de beheerslast die nodig is om ze te gebruiken.—>
