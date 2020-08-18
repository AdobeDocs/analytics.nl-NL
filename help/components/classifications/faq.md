---
title: Veelgestelde vragen over classificaties
description: Veelgestelde vragen over classificaties.
translation-type: tm+mt
source-git-commit: 0870ace3fea8e3ef650d2de2960006a0d655cf9f
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# Veelgestelde vragen over classificaties

Veelgestelde vragen over classificaties.

## Hoe classificeer ik afmetingspunt &quot;0&quot;?

Classificatiebestanden die zijn geüpload met een sleutelwaarde of classificatiewaarde nul (`0`), resulteren in een fout. Het omvat alle waarden die slechts nul (`00`, `000`, etc.) bevatten. Er zijn verschillende methoden om dit probleem op te lossen:

* **Alternatieve waarden** implementeren: Het gebruik van een andere tekstwaarde dan `"0"` is de beste en eenvoudigste manier om dit probleem op te lossen. Wijzig bijvoorbeeld `s.campaign = "0";` de implementatie in `s.campaign = "Zero";`.

* **Verwerkingsregels** gebruiken: U kunt afmetingspunten tussen gegevensinzameling en hun opslag in een rapportreeks wijzigen. Maak de volgende verwerkingsregel:

   *Als de[dimensie]gelijk is`0`, overschrijft u de waarde van de[dimensie]met de aangepaste waarde`Zero`.*

* **Een VISTA-regel** aanvragen: Een consultant van de Diensten van de Techniek plaatst - omhoog een server-zijregel voor u tegen extra kosten. Neem contact op met de accountmanager van uw organisatie om een VISTA-regel aan te vragen.

## Kan ik de classificatieimporteur gebruiken om dimensie-items in te delen die nog niet bestaan?

Ja, *nochtans tellen het doen dit elk afmeting punt als factureerbare servervraag.*

* Dimension-objecten die al bestaan, brengen geen extra kosten met zich mee.
* Het gebruik van de builder van de classificatieregel classificeert geen niet-bestaande items en brengt daarom geen extra kosten met zich mee.

## Hoe classificeer ik waarden die speciale karakters bevatten?

Het gebruik van speciale tekens zoals komma&#39;s of dubbele aanhalingstekens in rapportage wordt doorgaans niet aanbevolen. In sommige gevallen is het gebruik ervan echter noodzakelijk. Als uw rapporteringswaarden dergelijke karakters bevatten die u verkiest om te classificeren, gebruik de volgende stappen:

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Classification importer]**.
2. Klik op het **[!UICONTROL Browser export]** tabblad.
3. Configureer de exportinstellingen en controleer of Offerteuitvoer NIET is geselecteerd.
4. Klik op het gedownloade bestand **[!UICONTROL Export File]** en open het in een spreadsheet-editor.
5. Zoek op regel 1 cel C1 op, die de waarde bevat `v:2.0`. Verander de waarde aan `v:2.1` en pas de gewenste classificaties op het werkboek toe.
6. Upload het bestand op dezelfde manier als elke andere classificatie.

## Wat zijn numerieke 2 classificaties?

Met numerieke 2 classificaties kunt u dimensie-items classificeren als op tijd gebaseerde metriek. In juli 2019 zijn ze uit de gebruikersinterface van Analytics geschrapt.
