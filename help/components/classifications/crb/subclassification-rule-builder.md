---
description: Gebruik subclassificaties met de bouwer van de classificatieregel.
title: Subclassificaties en de Bouwer van de Regel
feature: Classifications
exl-id: 745d6149-bcb1-48ad-abbe-63a9d009fa27
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 1%

---

# Subclassificaties en de regelbouwer (verouderd)

U kunt de Bouwer van de Regel van de Classificatie met sub-classificaties combineren als u ervoor zorgt dat elke subclassificatie een ouderwaarde heeft.

Het combineren van de functie voor classificatieregel met subclassificaties kan het beheer van classificaties vereenvoudigen en het aantal vereiste regels verminderen. Dit kan handig zijn als uw code voor bijhouden bestaat uit codes die u afzonderlijk wilt classificeren.

Zie [ Subclassificaties ](/help/components/classifications/importer/subclassifications.md) voor conceptuele informatie over sub-classificaties.

## Voorbeeld

Stel de volgende code in:

`channel:broad_campaign:creative`

Met een classificatiehiërarchie kunt u een classificatie toepassen op een classificatie (ook wel *`sub-classification`* genoemd). Dit betekent dat u de importer kunt gebruiken als een relationele database, met meerdere tabellen. In de ene tabel worden volledige volgcodes toegewezen aan sleutels en in de andere tabel worden deze codes toegewezen aan andere tabellen.

![](assets/sub_class_table.png)

Nadat u deze structuur op zijn plaats hebt, kunt u de [ Bouwer van de Regel van Classificaties ](/help/components/classifications/crb/classification-rule-builder.md) gebruiken om kleine dossiers te uploaden die slechts de raadplegingslijsten (de groene en rode lijsten in het voorafgaande beeld) bijwerken. Dan, kunt u de regelbouwer gebruiken om de belangrijkste classificatielijst bijgewerkt te houden.

In de volgende taak wordt beschreven hoe u dit kunt doen.

## Subclassificaties instellen met de Rule Builder

De stappen van het voorbeeld die beschrijven hoe u subclassificaties kunt uploaden gebruikend de Bouwer van de Regel.

1. Classificaties en subclassificaties maken in het classificatiebeheer.

   Voorbeeld:

   ![ Info van de Stap ](/help/admin/admin/assets/sub_class_create.png)

1. In de [ bouwer van de classificatieregel van Classificaties ](/help/components/classifications/crb/classification-rule-builder.md), classificeer de sub-classificatiesleutel van de originele volgende code.

   U voert dit uit gebruikend een regelmatige uitdrukking. In dit voorbeeld gebruikt de regel om *`Broad Campaign code`* te vullen deze reguliere expressie:

   | `#` | Type regel | Overeenkomst | Classificatie instellen | Naar |
   |---|---|---|---|---|
   |   | Gewone uitdrukking | `[^\:]:([^\:]):([^\:])` | Code brede campagne | `$1` |
   |   | Gewone uitdrukking | `[^\:]:([^\:]):([^\:])` | Creative-code | `$2` |

   >[!NOTE]
   >
   >U vult nu de subclassificaties *`Campaign Type`* en *`Campaign Director`* niet in.

1. Upload een classificatiebestand dat alleen de opgegeven subclassificaties bevat.

   Zie [ Veelvoudige Classificaties ](/help/components/classifications/importer/subclassifications.md).

   Voorbeeld:

   | Sleutel | Kanaal | Code brede campagne | Code&amp;amp voor uitgebreide campagne;Hoed;Type campagne | Code&amp;amp voor uitgebreide campagne;Hoed;Campagne Director | ... |
   |---|---|---|---|---|---|
   | &#42; |  | 111 | Merk | Suzanne |  |
   | &#42; |  | 222 | Merk | Frank |  |

1. Upload een klein bestand (zoals hierboven weergegeven) om de opzoektabellen te onderhouden.

   U kunt dit bestand bijvoorbeeld uploaden wanneer een nieuwe *`Broad Campaign code`* wordt geïntroduceerd. Dit bestand is van toepassing op eerder geclassificeerde waarden. En als u een nieuwe subclassificatie maakt (zoals *`Creative Theme`* als een subclassificatie van *`Creative code`* ), uploadt u alleen het bestand voor de subclassificatie in plaats van het volledige classificatiebestand.

   Voor de rapportage van deze subclassificaties werken deze precies op de bovenste classificaties. Dit vermindert de beheerslast die nodig is om ze te gebruiken.
