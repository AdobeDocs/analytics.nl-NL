---
description: Stappen die beschrijven hoe classificatiegegevens moeten worden verwijderd of verwijderd.
subtopic: Classifications
title: Classificatiegegevens verwijderen
topic: Admin tools
uuid: 5b1b0ac7-ee52-4fd8-b98e-25283595cf0c
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Classificatiegegevens verwijderen

Soms is het nodig om classificatiegegevens te verwijderen nadat deze zijn geüpload. Gebruik `~empty~` of `~deletekey~`, afhankelijk van wat u wilt verwijderen.

## Stappen om classificatiegegevens te verwijderen

Wanneer classificatiegegevens worden verwijderd, moet een classificatiebestand met `~empty~` of `~deletekey~` in de juiste cellen worden geüpload.

1. Klik op **[!UICONTROL Admin]** > **[!UICONTROL Classification Importer]**.
1. Klik op **[!UICONTROL Browser Export]**.
1. Selecteer de rapportsuite en gegevensset waarvan u classificatiegegevens wilt verwijderen.
1. Pas optionele instellingen aan om specifieke gegevens te filteren die u zoekt en klik vervolgens op **[!UICONTROL Export File]**.
1. Nadat het bestand is gedownload, opent u het bestand en vervangt u eventuele classificatiewaarden door `~empty~` of `~deletekey~`.
1. Sla het bestand op als een tekstbestand met tabs als scheidingsteken.
1. Klik **[!UICONTROL Import File]** en upload het opgeslagen classificatiebestand weer naar Adobe Analytics.

## Een afzonderlijke classificatiewaarde verwijderen

Meerdere classificaties kunnen tot dezelfde variabele behoren. U kunt bijvoorbeeld twee verschillende classificaties van eVar1 hebben. Als u slechts één geclassificeerde waarde wilt verwijderen, vervangt u de indelingswaarde door `~empty~`. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam Naam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~empty~` |

Bij gebruik `~empty~` onder de categorie Inventaris blijven de gegevens voor de categorie Naam inventarisatie behouden. Met de `~empty~` waarde worden alleen classificatiegegevens voor die cel verwijderd.

## Een volledige classificatieregel verwijderen

Gebruik deze optie `~deletekey~` in een willekeurige kolom om de volledige indelingsrij te verwijderen. Bijvoorbeeld:

| Inventaris SKU (eVar8) | Fantasienaam Naam | Inventariscategorie |
| --- | --- | --- |
| 857467 | V-neksweater | Vrouwelijke kleding |
| 948203 | Enkel haakje | Juwelen |
| 174391 | Witte corduroyans | `~deletekey~` |

Door gebruik te maken `~deletekey~` van de categorie Inventaris worden alle classificatiegegevens voor de hoofdwaarde verwijderd `174391`. Het wordt alsof de rij nooit geclassificeerd is.

## Punten en uiteinden

* Als u `~deletekey~`het classificatiebestand gebruikt, hebt u er slechts één per rij voor nodig.
* `~empty~` en `~deletekey~` moeten *exacte* overeenkomsten zijn. Spaties of hoofdletters zijn niet toegestaan.
* U kunt geen waarden verwijderen uit de sleutelkolom. Deze waarden worden rechtstreeks aan de variabele doorgegeven en zijn permanent.
* Als u een classificatiewaarde verwijdert die subclassificaties heeft, worden deze subclassificaties ook verwijderd. Classificaties kunnen niet bestaan zonder een sleutelwaarde en het bovenliggende element van een subclassificatie is de hoofdwaarde ervan.
* Het is mogelijk om gegevens van subclassificaties te verwijderen terwijl de bovenliggende classificatie intact blijft.
