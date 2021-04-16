---
description: Stappen die beschrijven hoe classificatiegegevens moeten worden verwijderd of verwijderd.
subtopic: Classifications
title: Classificatiedata verwijderen
feature: Admin Tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
exl-id: 2b156e66-3090-4048-8192-a412320e3be3
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 5%

---

# Classificatiedata verwijderen

Soms is het nodig om classificatiegegevens te verwijderen nadat deze zijn geüpload. Gebruik `~empty~` of `~deletekey~`, afhankelijk van wat u wilt verwijderen.

## Stappen om classificatiegegevens te verwijderen

Wanneer u classificatiegegevens verwijdert, uploadt u een classificatiebestand met `~empty~` of `~deletekey~` in de juiste cellen.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klik op **[!UICONTROL Browser Export]**.
1. Selecteer de rapportsuite en gegevensset waarvan u classificatiegegevens wilt verwijderen.
1. Pas om het even welke facultatieve montages aan filter specifieke gegevens aan u zoekt, dan klik **[!UICONTROL Export File]**.
1. Nadat het bestand is gedownload, opent u het bestand en vervangt u eventuele classificatiewaarden door `~empty~` of `~deletekey~`.
1. Sla het bestand op als een tekstbestand met tabs als scheidingsteken.
1. Klik op **[!UICONTROL Import File]** en upload het opgeslagen classificatiebestand weer naar Adobe Analytics.

## Een afzonderlijke classificatiewaarde verwijderen

Meerdere classificaties kunnen tot dezelfde variabele behoren. U kunt bijvoorbeeld twee verschillende classificaties van eVar1 hebben. Als u slechts één geclassificeerde waarde wilt verwijderen, vervangt u de classificatiewaarde door `~empty~`. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam Naam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~empty~` |

Als u `~empty~` gebruikt onder de categorie Inventaris, blijven de gegevens voor de categorie Naam inventarisatie behouden. Met de waarde `~empty~` worden alleen classificatiegegevens voor die cel verwijderd.

## Een volledige classificatieregel verwijderen

Gebruik `~deletekey~` in om het even welke kolom om de volledige classificatierij te schrappen. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam Naam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~deletekey~` |

Als u `~deletekey~` gebruikt onder de categorie Inventaris, worden alle classificatiegegevens voor de hoofdwaarde `174391` verwijderd. Het wordt alsof de rij nooit geclassificeerd is.

## Punten en uiteinden

* Als u `~deletekey~` gebruikt, hebt u slechts één per rij in een classificatiebestand nodig.
* `~empty~` en  `~deletekey~` moet  ** exactmatch zijn. Spaties of hoofdletters zijn niet toegestaan.
* U kunt geen waarden verwijderen uit de sleutelkolom. Deze waarden worden rechtstreeks aan de variabele doorgegeven en zijn permanent.
* Als u een classificatiewaarde verwijdert die subclassificaties heeft, worden deze subclassificaties ook verwijderd. Classificaties kunnen niet bestaan zonder een sleutelwaarde en het bovenliggende element van een subclassificatie is de hoofdwaarde ervan.
* Het is mogelijk om gegevens van subclassificaties te verwijderen terwijl de bovenliggende classificatie intact blijft.
