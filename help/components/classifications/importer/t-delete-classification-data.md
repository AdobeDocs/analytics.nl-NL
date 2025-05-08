---
description: Stappen die beschrijven hoe classificatiegegevens moeten worden verwijderd of verwijderd.
title: Classificatiegegevens verwijderen
feature: Classifications
exl-id: 2b156e66-3090-4048-8192-a412320e3be3
source-git-commit: a40f30bbe8fdbf98862c4c9a05341fb63962cdd1
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 3%

---

# Classificatiegegevens verwijderen

Soms is het nodig om classificatiegegevens te verwijderen nadat deze zijn geüpload. Gebruik `~empty~` of `~deletekey~` , afhankelijk van wat u wilt verwijderen.

## Stappen om classificatiegegevens te verwijderen

Wanneer u classificatiegegevens verwijdert, uploadt u een classificatiebestand met `~empty~` of `~deletekey~` in de juiste cellen.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]** .
1. Klik op **[!UICONTROL Browser Export]**.
1. Selecteer de rapportsuite en gegevensset waarvan u classificatiegegevens wilt verwijderen.
1. Pas eventuele optionele instellingen aan om specifieke gegevens te filteren die u zoekt en klik vervolgens op **[!UICONTROL Export File]** .
1. Nadat het bestand is gedownload, opent u het bestand en vervangt u eventuele classificatiewaarden door `~empty~` of `~deletekey~` .
1. Sla het bestand op als een tekstbestand met tabs als scheidingsteken.
1. Klik op **[!UICONTROL Import File]** en upload het opgeslagen classificatiebestand weer naar Adobe Analytics.

## Een afzonderlijke classificatiewaarde verwijderen

Meerdere classificaties kunnen tot dezelfde variabele behoren. U kunt bijvoorbeeld twee verschillende classificaties van eVar1 hebben. Als u slechts één geclassificeerde waarde wilt verwijderen, vervangt u de classificatiewaarde door `~empty~` . Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~empty~` |

Als u `~empty~` gebruikt onder de categorie Inventaris, blijven de gegevens voor de categorie Naam inventarisatie behouden. Met de waarde `~empty~` worden alleen classificatiegegevens voor die cel verwijderd.

## Een volledige classificatieregel verwijderen

Gebruik `~deletekey~` in een willekeurige kolom om de volledige indelingsrij te verwijderen. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~deletekey~` |

Als u `~deletekey~` gebruikt onder de categorie Inventaris, worden alle classificatiegegevens voor de sleutelwaarde `174391` verwijderd. Het wordt alsof de rij nooit geclassificeerd is.

## Pekken en uiteinden

* Als u `~deletekey~` gebruikt, hebt u slechts één per rij in een classificatiebestand nodig.
* `~empty~` en `~deletekey~` moeten *nauwkeurige* gelijken zijn. Spaties of hoofdletters zijn niet toegestaan.
* U kunt geen waarden verwijderen uit de sleutelkolom. Deze waarden worden rechtstreeks aan de variabele doorgegeven en zijn permanent.
* Als u een classificatiewaarde verwijdert die subclassificaties heeft, worden deze subclassificaties ook verwijderd. Classificaties kunnen niet bestaan zonder een sleutelwaarde en het bovenliggende element van een subclassificatie is de hoofdwaarde ervan.
* Het is mogelijk om gegevens van subclassificaties te verwijderen terwijl de bovenliggende classificatie intact blijft.
