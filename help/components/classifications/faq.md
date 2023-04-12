---
title: Veelgestelde vragen over classificaties
description: Veelgestelde vragen over classificaties.
feature: Classifications
exl-id: e929d7cb-0bfd-46de-88d1-aea2b4b91911
source-git-commit: 34ba0e09cd909951a777b0ad3da080958633f97e
workflow-type: tm+mt
source-wordcount: '365'
ht-degree: 0%

---

# Veelgestelde vragen over classificaties

Veelgestelde vragen over classificaties.

## Hoe classificeer ik afmetingspunt &quot;0&quot;?

Classificatiebestanden geüpload met een sleutelwaarde of classificatiewaarde nul (`0`) resulteert in een fout. Het omvat alle waarden die slechts nul bevatten (`00`, `000`, enzovoort). Er zijn verschillende methoden om dit probleem op te lossen:

* **Alternatieve waarden implementeren**: Een andere tekstwaarde gebruiken dan `"0"` is de beste en eenvoudigste manier om dit probleem op te lossen. Bijvoorbeeld, wijzigen `s.campaign = "0";` in uw implementatie naar `s.campaign = "Zero";`.

* **Verwerkingsregels gebruiken**: U kunt afmetingspunten tussen gegevensinzameling en hun opslag in een rapportreeks wijzigen. Maak de volgende verwerkingsregel:

   *Indien [dimensie] equals `0`, overschrijf de waarde van [dimensie] met aangepaste waarde `Zero`.*

* **Een VISTA-regel aanvragen**: Een consultant van de Diensten van de Techniek plaatst - omhoog een server-zijregel voor u tegen extra kosten. Neem contact op met het accountteam van Adobe om een VISTA-regel aan te vragen.

## Kan ik de classificatieimporteur gebruiken om dimensie-items in te delen die nog niet bestaan?

Ja, *nochtans telt het doen dit elk afmetingspunt als factureerbare servervraag.*

* Dimension-objecten die al bestaan, brengen geen extra kosten met zich mee.
* Het gebruik van de builder van de classificatieregel classificeert geen niet-bestaande items en brengt daarom geen extra kosten met zich mee.

## Hoe classificeer ik waarden die speciale karakters bevatten?

Het gebruik van spaties met regelafstand en navolgende in classificatiegegevens en raakgegevens wordt niet ondersteund omdat Adobe Analytics de lege tekens uit deze gegevens afkapt.

Het gebruik van speciale tekens zoals komma&#39;s of dubbele aanhalingstekens in rapportage wordt doorgaans niet aanbevolen. In sommige gevallen is het gebruik ervan echter noodzakelijk. Voer de volgende stappen uit als uw rapportwaarden tekens bevatten die u wilt classificeren:

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Classification importer]**.
2. Klik op de knop **[!UICONTROL Browser export]** tab.
3. Configureer de exportinstellingen en controleer of Offerteuitvoer NIET is geselecteerd.
4. Klikken **[!UICONTROL Export File]** en opent u het gedownloade bestand in een spreadsheet-editor.
5. Zoek op regel 1 cel C1 op, die de waarde bevat `v:2.0`. De waarde wijzigen in `v:2.1` en past de gewenste classificaties op het werkboek toe.
6. Upload het bestand op dezelfde manier als elke andere classificatie.

## Wat zijn numerieke 2 classificaties?

Met numerieke 2 classificaties kunt u dimensie-items classificeren als op tijd gebaseerde metriek. In juli 2019 zijn ze uit de gebruikersinterface van Adobe Analytics teruggetreden.
