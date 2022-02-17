---
description: Stappen die beschrijven hoe classificatiegegevens moeten worden verwijderd of verwijderd.
title: Classificatiedata verwijderen
feature: Classifications
exl-id: 2b156e66-3090-4048-8192-a412320e3be3
source-git-commit: 35413ac43eed5ab7218794f26e4753acf08f18ee
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 5%

---

# Classificatiedata verwijderen

Soms is het nodig om classificatiegegevens te verwijderen nadat deze zijn geüpload. Gebruik beide `~empty~` of `~deletekey~`, afhankelijk van wat u wilt verwijderen.

## Stappen om classificatiegegevens te verwijderen

Wanneer classificatiegegevens worden verwijderd, wordt een classificatiebestand geüpload dat een `~empty~` of `~deletekey~` in de desbetreffende cellen.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klik op **[!UICONTROL Browser Export]**.
1. Selecteer de rapportsuite en gegevensset waarvan u classificatiegegevens wilt verwijderen.
1. Pas optionele instellingen aan om specifieke gegevens te filteren die u zoekt, en klik vervolgens op **[!UICONTROL Export File]**.
1. Nadat het bestand is gedownload, opent u het bestand en vervangt u eventuele classificatiewaarden door een van de volgende `~empty~` of `~deletekey~`.
1. Sla het bestand op als een tekstbestand met tabs als scheidingsteken.
1. Klikken **[!UICONTROL Import File]** en uploadt u het opgeslagen classificatiebestand terug naar Adobe Analytics.

## Een afzonderlijke classificatiewaarde verwijderen

Meerdere classificaties kunnen tot dezelfde variabele behoren. U kunt bijvoorbeeld twee verschillende classificaties van eVar1 hebben. Als u slechts één geclassificeerde waarde wilt verwijderen, vervangt u de indelingswaarde door `~empty~`. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam Naam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~empty~` |

Gebruiken `~empty~` onder de classificatie van de Categorie Overzicht blijven de gegevens voor de classificatie van Naam Inventaris behouden. De `~empty~` Met deze waarde worden alleen classificatiegegevens voor die cel verwijderd.

## Een volledige classificatieregel verwijderen

Gebruiken `~deletekey~` in om het even welke kolom om de volledige classificatierij te schrappen. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam Naam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~deletekey~` |

Gebruiken `~deletekey~` onder de categorie Inventaris worden alle classificatiegegevens voor de hoofdwaarde verwijderd `174391`. Het wordt alsof de rij nooit geclassificeerd is.

## Punten en uiteinden

* Als u `~deletekey~`, hebt u slechts één code per rij in een classificatiebestand nodig.
* `~empty~` en `~deletekey~` moet *exact* overeenkomsten. Spaties of hoofdletters zijn niet toegestaan.
* U kunt geen waarden verwijderen uit de sleutelkolom. Deze waarden worden rechtstreeks aan de variabele doorgegeven en zijn permanent.
* Als u een classificatiewaarde verwijdert die subclassificaties heeft, worden deze subclassificaties ook verwijderd. Classificaties kunnen niet bestaan zonder een sleutelwaarde en het bovenliggende element van een subclassificatie is de hoofdwaarde ervan.
* Het is mogelijk om gegevens van subclassificaties te verwijderen terwijl de bovenliggende classificatie intact blijft.
