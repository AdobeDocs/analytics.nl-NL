---
title: Veelgestelde vragen over classificaties
description: Veelgestelde vragen over classificaties.
translation-type: tm+mt
source-git-commit: a63b8ae3948ffd9a37058696aa1b1d4c923709ba
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# Veelgestelde vragen over classificaties

Veelgestelde vragen over classificaties.

## Hoe classificeer ik afmetingspunt &quot;0&quot;?

Classificatiebestanden die zijn geüpload met een sleutelwaarde of classificatiewaarde nul (`0`), resulteren in een fout. Het omvat alle waarden die slechts nul (`00`, `000`, etc.) bevatten. Er zijn verschillende methoden om dit probleem op te lossen:

* **Alternatieve waarden** implementeren: Het gebruik van een andere tekstwaarde dan  `"0"` is de beste en eenvoudigste manier om dit probleem op te lossen. Wijzig `s.campaign = "0";` in uw implementatie bijvoorbeeld in `s.campaign = "Zero";`.

* **Verwerkingsregels** gebruiken: U kunt afmetingspunten tussen gegevensinzameling en hun opslag in een rapportreeks wijzigen. Maak de volgende verwerkingsregel:

   *Als  [] afmetingen gelijk zijn  `0`, overschrijft u de waarde van de  [] dimensie met de aangepaste waarde  `Zero`.*

* **Een VISTA-regel** aanvragen: Een consultant van de Diensten van de Techniek plaatst - omhoog een server-zijregel voor u tegen extra kosten. Neem contact op met de accountmanager van uw organisatie om een VISTA-regel aan te vragen.

## Kan ik de classificatieimporteur gebruiken om dimensie-items in te delen die nog niet bestaan?

Ja, *maar daarbij telt u elk dimensie-item als een factureerbare serveraanroep.*

* Dimension-objecten die al bestaan, brengen geen extra kosten met zich mee.
* Het gebruik van de builder van de classificatieregel classificeert geen niet-bestaande items en brengt daarom geen extra kosten met zich mee.

## Hoe classificeer ik waarden die speciale karakters bevatten?

Het gebruik van speciale tekens zoals komma&#39;s of dubbele aanhalingstekens in rapportage wordt doorgaans niet aanbevolen. In sommige gevallen is het gebruik ervan echter noodzakelijk. Voer de volgende stappen uit als uw rapportwaarden tekens bevatten die u wilt classificeren:

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Classification importer]**.
2. Klik op het tabblad **[!UICONTROL Browser export]**.
3. Configureer de exportinstellingen en controleer of Offerteuitvoer NIET is geselecteerd.
4. Klik **[!UICONTROL Export File]**, en open het gedownloade dossier in een spreadsheetredacteur.
5. Zoek op regel 1 cel C1 op, die de waarde `v:2.0` bevat. Verander de waarde in `v:2.1` en pas de gewenste classificaties op het werkboek toe.
6. Upload het bestand op dezelfde manier als elke andere classificatie.

## Wat zijn numerieke 2 classificaties?

Met numerieke 2 classificaties kunt u dimensie-items classificeren als op tijd gebaseerde metriek. In juli 2019 zijn ze uit de gebruikersinterface van Adobe Analytics teruggetreden.
