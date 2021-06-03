---
title: Adobe Analytics implementeren in een ontwikkelomgeving
description: Leer hoe u Adobe Experience Platform Launch kunt gebruiken om Adobe Analytics in uw ontwikkelomgeving te implementeren.
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
source-git-commit: f669af03a502d8a24cea3047b96ec7cba7c59e6f
workflow-type: tm+mt
source-wordcount: '544'
ht-degree: 1%

---

# Implementeer een analytische implementatie in een ontwikkelomgeving

Nadat een eigenschap is gemaakt en geconfigureerd in Launch, kunnen de bibliotheken worden geïmplementeerd en kan de code op uw site worden geïmplementeerd.

## Vereisten

[Een eigenschap maken en configureren voor Adobe Analytics in Launch](create-analytics-property.md): Open het hulpprogramma en maak ruimte voor de implementatie van Analytics.

## adapters en omgevingen maken

De lancering past vele organisatorische werkschema&#39;s in het opstellen van code aan. Ga als volgt te werk om de minimaal vereiste componenten voor een analytische implementatie te maken. Als beheerder van de Lancering, kunt u binnen uw organisatie werken om het correcte werkschema voor het opstellen van de oplossingen van Adobe te vestigen.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
2. Klik op de eigenschap Starten die u op uw site wilt implementeren.
3. Klik op het tabblad Adapters en klik vervolgens op Adapter toevoegen.
4. Geef deze de naam &quot;Akamai&quot; en selecteer Akamai in het vervolgkeuzemenu type. Klik op Opslaan.
5. Ga naar het tabblad Omgevingen en klik vervolgens op Nieuwe omgeving maken.
6. Selecteer Ontwikkeling, noem het &quot;Milieu Dev&quot;, dan selecteer de adapter Akamai van dropdown. Klik op Maken en vervolgens op Sluiten.
7. Klik op Omgeving toevoegen, selecteer Staging, geef deze de naam &quot;Staging Environment&quot; en selecteer vervolgens de Akamai-adapter. Klik op Maken en vervolgens op Sluiten.
8. Klik nogmaals op Omgeving toevoegen, selecteer Productie, geef deze de naam &quot;Productomgeving&quot; en selecteer de Akamai-adapter. Klik op Maken en vervolgens op Sluiten.

## Een ontwikkelbibliotheek maken

Ondanks alle tot dusver aangebrachte wijzigingen en configuraties is er geen code gepubliceerd. Als u een bibliotheek maakt die ruwweg is vertaald als een verzameling wijzigingen, kunt u code publiceren die op uw site wordt gebruikt.

1. Ga naar [Adobe Experience Platform Launch](https://launch.adobe.com) en meld u aan als u hierom wordt gevraagd.
2. Klik op de eigenschap Starten die u op uw site wilt implementeren.
3. Klik op het tabblad Publiceren en klik vervolgens op Nieuwe bibliotheek toevoegen.
4. Geef de bibliotheek de naam &#39;Aanvankelijke wijzigingen&#39; en selecteer de ontwikkelomgeving.
5. Klik op Alle gewijzigde bronnen toevoegen. Hierin worden automatisch Adobe Analytics, Identity Service en Core vermeld.
6. Klik op Opslaan.
7. Klik op het scherm met de publicatieworkflow op het vervolgkeuzemenu naast de nieuwe bibliotheek en klik op Samenstellen voor ontwikkeling. Na een paar seconden wordt de gele stip in de bibliotheek groen om aan te geven dat het samenstellen is gelukt.
8. Ga naar het tabblad Milieu en klik vervolgens op de ontwikkelomgeving.
9. Kopieer onder &#39;Start installeren&#39; de codeblokken en geef deze door aan de eigenaars van de website van uw organisatie.

## Starten installeren in de ontwikkelomgeving van uw website

Als u de code van uw website beheert, implementeert u de twee codeblokken op hun respectievelijke locaties (in de tag `<head>` en net boven de afsluitende tag `</body>`) op elke pagina van uw site. Deze code wordt algemeen geplaatst in het overkoepelende malplaatje van de plaats. Een lege pagina die alleen implementatiecode bevat, ziet er als volgt uit:

```html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Example page</title>
  <script src="//assets.adobedtm.com/launch-xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx-development.min.js"></script>
</head>
<body>
   <p>This is a test page.</p>
   <script type="text/javascript">_satellite.pageBottom();</script>
</body>
</html>
```

## Problemen oplossen

**Poging om samen te stellen mislukt.**

Een algemene reden is dat er al elementen bestaan in andere bibliotheken die worden geduwd op staging of productie. Zorg ervoor dat bij het maken van bibliotheken alleen gewijzigde bronnen aan de bibliotheek worden toegevoegd.

## Documentatie en aanvullende middelen

- [Aan de slag met starten](https://experienceleague.adobe.com/docs/launch/using/intro/get-started/quick-start.html): Meer informatie over de basisworkflow van Launch
- [Publicatie](https://experienceleague.adobe.com/docs/launch/using/reference/publish/overview.html) starten: Meer informatie over publiceren en omgevingen

## Volgende stappen

[Valideer uw analytische implementatie en publiceer naar productie](validate-publish-prod.md): Begin waarde uit Adobe Analytics te halen.
