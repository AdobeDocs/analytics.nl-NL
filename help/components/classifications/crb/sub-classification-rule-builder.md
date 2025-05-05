---
description: U kunt de Classification Rule Builder niet combineren met subclassificaties.
title: Subclassificaties en de Rule Builder
feature: Classifications
exl-id: 745d6149-bcb1-48ad-abbe-63a9d009fa27
source-git-commit: e7346b11a7d3eb4c18ec02df6c8a07574e02a2b4
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 3%

---

# Subclassificaties en de Rule Builder

U kunt de Bouwer van de Regel van de Classificatie met sub-classificaties combineren als u ervoor zorgt dat elke subclassificatie een ouderwaarde heeft.

Het combineren van de functie voor classificatieregel met subclassificaties kan het beheer van classificaties vereenvoudigen en het aantal vereiste regels verminderen. Dit kan handig zijn als uw code voor bijhouden bestaat uit codes die u afzonderlijk wilt classificeren.

Zie [Subclassificaties](/help/components/classifications/c-sub-classifications.md) voor conceptuele informatie over subclassificaties.

## Voorbeeld

Stel de volgende code in:

`channel:broad_campaign:creative`

Met een classificatiehiërarchie kunt u een classificatie toepassen op een classificatie (ook wel *`sub-classification`*). Dit betekent dat u de importer kunt gebruiken als een relationele database, met meerdere tabellen. In de ene tabel worden volledige volgcodes toegewezen aan sleutels en in de andere tabel worden deze codes toegewezen aan andere tabellen.

![](assets/sub_class_table.png)

Nadat u deze structuur hebt ingesteld, kunt u de opdracht [Classifications Rule Builder](/help/components/classifications/crb/classification-rule-builder.md) om kleine dossiers te uploaden die slechts de raadplegingslijsten (de groene en rode lijsten in het voorafgaande beeld) bijwerken. Dan, kunt u de regelbouwer gebruiken om de belangrijkste classificatielijst bijgewerkt te houden.

De volgende taak beschrijft hoe te om dit te verwezenlijken.

## Subclassificaties instellen met de Rule Builder{#task_2D9016D8B4E84DBDAF88555E5369546F}

De stappen van het voorbeeld die beschrijven hoe u sub-classificaties kunt uploaden gebruikend de Bouwer van de Regel.

>[!NOTE]
>
>In deze stappen wordt beschreven hoe u het in [Subclassificaties en de Rule Builder](/help/components/classifications/crb/sub-classification-rule-builder.md).

1. Classificaties en subclassificaties maken in de [Classificatiebeheer](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=nl-NL).

   Voorbeeld:

   ![Stapinfo](/help/admin/admin/assets/sub_class_create.png)

1. In de [Classifications Rule Builder](/help/components/classifications/crb/classification-rule-builder.md), classificeert u de subclassificatiesleutel van de oorspronkelijke trackingcode.

   U voert dit uit gebruikend een regelmatige uitdrukking. In dit voorbeeld wordt de regel voor vullen *`Broad Campaign code`* zou deze reguliere expressie gebruiken:

   | `#` | Type regel | Overeenkomst | Classificatie instellen | Naar |
   |---|---|---|---|---|
   |  | Gewone uitdrukking | `[^\:]:([^\:]):([^\:]`) | Code brede campagne | `$1` |
   |  | Gewone uitdrukking | `[^\:]:([^\:]):([^\:]`) | Creatieve code | `$2` |

   >[!NOTE]
   >
   >U vult nu de subclassificaties niet in *`Campaign Type`* en *`Campaign Director`*.

1. Upload een classificatiebestand dat alleen de opgegeven subclassificaties bevat.

   Zie [Classificaties op meerdere niveaus](/help/components/classifications/c-sub-classifications.md).

   Voorbeeld:

   | Sleutel | Kanaal | Code brede campagne | Code&amp;hoed voor brede campagne;Type campagne | Code&amp;hoed voor uitgebreide campagne;Campagne voor Director | ... |
   |---|---|---|---|---|---|
   | &#42; |  | 111 | Merk | Suzanne |  |
   | &#42; |  | 222 | Merk | Frank |  |

1. Upload een klein bestand (zoals hierboven weergegeven) om de opzoektabellen te onderhouden.

   U kunt dit bestand bijvoorbeeld uploaden wanneer u een nieuw bestand *`Broad Campaign code`* wordt ingevoerd. Dit bestand is van toepassing op eerder geclassificeerde waarden. En als u een nieuwe subclassificatie maakt (zoals *`Creative Theme`* als een subclassificatie van *`Creative code`*) uploadt u alleen het bestand voor de subclassificatie in plaats van het hele classificatiebestand.

   Voor de rapportage van deze subclassificaties werken deze precies op de bovenste classificaties. Dit vermindert de beheerslast die nodig is om ze te gebruiken.-->
