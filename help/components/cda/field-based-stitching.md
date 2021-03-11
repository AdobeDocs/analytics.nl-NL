---
title: Veldgebaseerde stitching
description: Begrijp de eerste vereisten en de beperkingen van het stitching van gegevens gebruikend op gebied-gebaseerde stitching.
translation-type: tm+mt
source-git-commit: 7b43c4ebbf9446507ab90a90e26c51635303dcc6
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 0%

---


# Veldgebaseerde stitching

Cross-Device Analytics biedt twee verschillende methoden om gegevens aan elkaar te koppelen. Deze methode vertrouwt op een variabele Analytics, zoals [prop](/help/implement/vars/page-vars/prop.md) of [eVar](/help/implement/vars/page-vars/evar.md), om een persoonsidentificatie te bevatten. Het gebruikt die variabele als basis om apparaten samen te verbinden.

## Vereisten die specifiek zijn voor veldomstandigheden

Als u Cross-Device Analytics wilt implementeren met behulp van op het veld gebaseerde stitching, is het volgende vereist. Werk met teams binnen uw organisatie en uw Adobe-accountmanager om ervoor te zorgen dat u aan alle volgende voorwaarden voldoet.

>[!IMPORTANT]
>
>Als niet aan alle voorwaarden wordt voldaan, kan het zijn dat u Cross-Device Analytics of slechte resultaten niet kunt inschakelen bij het koppelen van gegevens.

* Alle voorwaarden die op [overzichtspagina](overview.md) worden vermeld.
* Uw implementatie moet een proxy of eVar instellen die een individu waar mogelijk op unieke wijze identificeert, bijvoorbeeld wanneer een gebruiker zich aanmeldt of een e-mail opent. Deze eis geldt voor alle platforms, inclusief mobiele apps indien gebruikt. Geef de gewenste identificatievariabele door aan uw accountmanager wanneer deze is ingericht voor stitching op basis van velden.

## Beperkingen die specifiek zijn voor stitching in het veld

* Veldgebaseerde stitching werkt het beste bij rapportsuites met een hoog gebruikersidentificatieniveau. Als uw rapportsuite een lage identificatie- of aanmeldfrequentie heeft, kunt u de [Co-op grafiek](device-graph.md) gebruiken.
* Hoewel props en eVars elk regels bevatten voor de manier waarop hoofdletters en kleine letters worden verwerkt voor rapportagedoeleinden, wordt door het stitching op basis van velden op geen enkele manier de eigenschap of eVar die voor stitching wordt gebruikt, getransformeerd. Op velden gebaseerde stitching gebruikt de waarde in het opgegeven veld omdat deze regels voor post VISTA en nabewerkingsregels bevat. Als bijvoorbeeld soms het woord &#39;Bob&#39; voorkomt in de pop/eVar en soms het woord &#39;BOB&#39; verschijnt, worden deze behandeld als twee aparte personen.

## Volgende stappen

Als uw organisatie aan alle vereisten voldoet en de beperkingen begrijpt, kunt u [Apparaatanalyse instellen](setup.md).
