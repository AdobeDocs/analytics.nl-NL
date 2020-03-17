---
description: U kunt de Classification Rule Builder combineren met subclassificaties om het classificatiebeheer te vereenvoudigen en het aantal vereiste regels te verminderen. Dit kan handig zijn als uw code voor bijhouden bestaat uit codes die u afzonderlijk wilt classificeren.
subtopic: Classifications
title: Subclassificaties en de Bouwer van de Regel - gebruiksgeval
topic: Admin tools
uuid: 6db6a4a9-b93c-413b-8049-1e6cc1ba4a38
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Subclassificaties en de Bouwer van de Regel - gebruiksgeval

U kunt de Classification Rule Builder combineren met subclassificaties om het classificatiebeheer te vereenvoudigen en het aantal vereiste regels te verminderen. Dit kan handig zijn als uw code voor bijhouden bestaat uit codes die u afzonderlijk wilt classificeren.

## Subclassificaties en de Bouwer van de Regel - gebruiksgeval {#concept_6C8672C242544D7487E82886BBFABE6E}

U kunt de Classification Rule Builder combineren met subclassificaties om het classificatiebeheer te vereenvoudigen en het aantal vereiste regels te verminderen. Dit kan handig zijn als uw code voor bijhouden bestaat uit codes die u afzonderlijk wilt classificeren.

Zie [Subclassificaties](/help/components/c-classifications2/c-sub-classifications.md) voor conceptuele informatie over subclassificaties.

**Voorbeeld**

Stel de volgende code in:

`channel:broad_campaign:creative`

Met een classificatiehiërarchie kunt u een classificatie toepassen op een classificatie ( *`sub-classification`* genaamd). Dit betekent dat u de importer kunt gebruiken als een relationele database, met meerdere tabellen. In de ene tabel worden volledige volgcodes toegewezen aan sleutels en in de andere tabel worden deze codes toegewezen aan andere tabellen.

![](assets/sub_class_table.png)

Nadat u deze structuur op zijn plaats hebt, kunt u de Bouwer [van de Regel van](/help/components/c-classifications2/crb/classification-rule-builder.md) Classificaties gebruiken om kleine dossiers te uploaden die slechts de raadplegingslijsten (de groene en rode lijsten in het voorafgaande beeld) bijwerken. Dan, kunt u de regelbouwer gebruiken om de belangrijkste classificatielijst bijgewerkt te houden.

De volgende taak beschrijft hoe te om dit te verwezenlijken.

## Subclassificaties instellen met de Rule Builder{#task_2D9016D8B4E84DBDAF88555E5369546F}

<!-- 

t_rule_builder_subclass.xml

 -->

De stappen van het voorbeeld die beschrijven hoe u sub-classificaties kunt uploaden gebruikend de Bouwer van de Regel.

>[!NOTE]
>
>Deze stappen beschrijven hoe te om het gebruiksgeval te verwezenlijken dat in [Subclassificaties en de Bouwer](/help/components/c-classifications2/crb/sub-classification-rule-builder.md)van de Regel wordt beschreven.

1. Classificaties en subclassificaties maken in het [classificatiebeheer](https://marketing.adobe.com/resources/help/en_US/reference/classifications.html).

   Voorbeeld:

   ![Stapinfo](assets/sub_class_create.png)

1. In de Bouwer [van de Regel van](/help/components/c-classifications2/crb/classification-rule-builder.md)Classificaties, classificeer de sub-classificatiesleutel van de originele het volgen code.

   U voert dit uit gebruikend een regelmatige uitdrukking. In dit voorbeeld *`Broad Campaign code`* zou de regel voor vullen deze reguliere expressie gebruiken:

   | `#` | Type regel | Overeenkomst | Classificatie instellen | Naar |
   |---|---|---|---|---|
   |  | Gewone uitdrukking | `[^\:]:([^\:]):([^\:]`) | Code brede campagne | `$1` |
   |  | Gewone uitdrukking | `[^\:]:([^\:]):([^\:]`) | Creatieve code | `$2` |

   >[!NOTE]
   >
   >U vult de subclassificaties nu niet in *`Campaign Type`* en *`Campaign Director`*.

1. Upload een classificatiebestand dat alleen de opgegeven subclassificaties bevat.

   Zie Classificaties op [meerdere niveaus](/help/components/c-classifications2/c-sub-classifications.md).

   Voorbeeld:

   | Sleutel | Kanaal | Code brede campagne | Code&amp;amp voor uitgebreide campagne;Hoed;Type campagne | Code&amp;amp voor uitgebreide campagne;Hoed;Campagne Director | ... |
   |---|---|---|---|---|---|
   | * |  | 111 | Merk | Suzanne |  |
   | * |  | 222 | Merk | Frank |  |

1. Upload een klein bestand (zoals hierboven weergegeven) om de opzoektabellen te onderhouden.

   U kunt dit bestand bijvoorbeeld uploaden wanneer er een nieuwe toepassing *`Broad Campaign code`* wordt geïntroduceerd. Dit bestand is van toepassing op eerder geclassificeerde waarden. En als u een nieuwe subclassificatie maakt (zoals *`Creative Theme`* een subclassificatie van *`Creative code`*), uploadt u alleen het bestand voor subclassificatie in plaats van het volledige classificatiebestand.

   Voor de rapportage van deze subclassificaties werken deze precies op de bovenste classificaties. Dit vermindert de beheerslast die nodig is om ze te gebruiken.
