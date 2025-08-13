---
title: Veelgestelde vragen over classificaties
description: Veelgestelde vragen over classificaties.
feature: Classifications
exl-id: e929d7cb-0bfd-46de-88d1-aea2b4b91911
source-git-commit: 4eea524bf95c9b6bc9ddc878c8c433bc1e60daee
workflow-type: tm+mt
source-wordcount: '410'
ht-degree: 0%

---

# Veelgestelde vragen over importmodule voor classificatie

{{classification-importer-deprecation}}

Veelgestelde vragen over het gebruik van de indelingsimporteur.

## Hoe classificeer ik afmetingspunt &quot;0&quot;?

Classificatiebestanden die zijn geüpload met een sleutelwaarde of een classificatiewaarde van nul (`0`), resulteren in een fout. Het omvat alle waarden die slechts nul (`00`, `000`, etc.) bevatten. Er zijn verschillende methoden om dit probleem op te lossen:

* **voer alternatieve waarden** uit: Het gebruiken van een tekstwaarde buiten `"0"` is de beste en gemakkelijkste manier om deze kwestie op te lossen. Wijzig `s.campaign = "0";` in uw implementatie bijvoorbeeld in `s.campaign = "Zero";` .

* **de verwerkingsregels van het Gebruik**: U kunt afmetingspunten tussen gegevensinzameling en hun opslag in een rapportreeks wijzigen. Maak de volgende verwerkingsregel:

  *als [ afmeting ] `0` evenaart, waarde van [ afmeting ] met douanewaarde `Zero` overschrijft.*

* **Verzoek een VISTA regel**: Een consultant van de Diensten van de Techniek plaatst - omhoog een server-zijregel voor u aan extra kosten. Neem contact op met uw Adobe-accountteam om een VISTA-regel aan te vragen.

## Kan ik de classificatieimporteur gebruiken om dimensie-items in te delen die nog niet bestaan?

Ja, *nochtans tellen het doen dit elk afmeting punt als factureerbare servervraag.*

* Dimension-objecten die al bestaan, brengen geen extra kosten met zich.
* Het gebruik van de builder van de classificatieregel classificeert geen niet-bestaande items en brengt daarom geen extra kosten met zich mee.

## Hoe classificeer ik waarden die speciale karakters bevatten?

Het gebruik van spaties met regelafstand en navolgende in classificatiegegevens en raakgegevens wordt niet ondersteund omdat Adobe Analytics automatisch lege tekens afkapt.

Het gebruik van speciale tekens zoals komma&#39;s of dubbele aanhalingstekens in rapportage wordt doorgaans niet aanbevolen. In sommige gevallen is het gebruik ervan echter noodzakelijk. Voer de volgende stappen uit als uw rapportwaarden tekens bevatten die u wilt classificeren:

1. Meld u aan bij Adobe Analytics en navigeer naar **[!UICONTROL Admin]** > **[!UICONTROL Classification importer]** .
2. Klik op de tab **[!UICONTROL Browser export]** .
3. Configureer de exportinstellingen en zorg ervoor dat Offerteuitvoer NIET is geselecteerd.
4. Klik op **[!UICONTROL Export File]** en open het gedownloade bestand in een spreadsheet-editor.
5. Zoek op regel 1 cel C1 op, die de waarde `v:2.0` bevat. Wijzig de waarde in `v:2.1` en pas de gewenste classificaties toe op het werkboek.
6. Upload het bestand op dezelfde manier als elke andere classificatie.

## Wat zijn numerieke 2 classificaties?

Met numerieke 2 classificaties kunt u dimensie-items classificeren als op tijd gebaseerde metriek. In juli 2019 zijn ze uit de gebruikersinterface van Adobe Analytics teruggetreden.

## Hoe kan ik gegevens uit een classificatiebestand verwijderen?

Omring het veld met speciale tekens tussen dubbele aanhalingstekens (`"`). Een dubbel aanhalingsteken kan in een beschermde cel verschijnen door het met twee dubbele aanhalingstekens (`" "`) te vervangen. Bijvoorbeeld:

```
My String "of data"
```

Geëxpandeerd zou zijn:

```
"My String ""of data"""
```
