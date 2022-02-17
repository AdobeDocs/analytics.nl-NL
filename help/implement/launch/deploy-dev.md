---
title: Adobe Analytics implementeren in een ontwikkelomgeving
description: Leer hoe u tags kunt gebruiken om Adobe Analytics in uw ontwikkelomgeving te implementeren.
feature: Launch Implementation
exl-id: 324943db-cb0b-40b1-8884-56bb3f608278
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Implementeer een analytische implementatie in een ontwikkelomgeving

Nadat u een eigenschap tag hebt gemaakt en geconfigureerd, kunnen de bibliotheken worden geïmplementeerd en kan de code op uw site worden geïmplementeerd.

>[!NOTE]
>Adobe Experience Platform Launch is omgedoopt tot een reeks technologieën voor gegevensverzameling in Experience Platform. Diverse terminologische wijzigingen zijn als gevolg hiervan in de productdocumentatie doorgevoerd. Raadpleeg het volgende [document](https://experienceleague.adobe.com/docs/experience-platform/tags/term-updates.html?lang=en) voor een geconsolideerde referentie van de terminologische wijzigingen.

## Vereisten

[Een eigenschap voor tags maken en configureren voor Adobe Analytics](create-analytics-property.md): Open het hulpprogramma en maak ruimte voor de implementatie van Analytics.

## adapters en omgevingen maken

De markeringen passen vele organisatorische werkschema&#39;s in het opstellen van code aan. Ga als volgt te werk om de minimaal vereiste componenten voor een analytische implementatie te maken. Als tagbeheerder kunt u binnen uw organisatie de juiste workflow voor het implementeren van Adobe-oplossingen instellen.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de eigenschap tag die u op uw site wilt implementeren.
3. Klik op het tabblad Adapters en klik vervolgens op Adapter toevoegen.
4. Geef deze de naam &quot;Akamai&quot; en selecteer Akamai in het vervolgkeuzemenu type. Klik op Opslaan.
5. Ga naar het tabblad Omgevingen en klik vervolgens op Nieuwe omgeving maken.
6. Selecteer Ontwikkeling, noem het &quot;Milieu Dev&quot;, dan selecteer de adapter Akamai van dropdown. Klik op Maken en vervolgens op Sluiten.
7. Klik op Omgeving toevoegen, selecteer Staging, geef deze de naam &quot;Staging Environment&quot; en selecteer vervolgens de Akamai-adapter. Klik op Maken en vervolgens op Sluiten.
8. Klik nogmaals op Omgeving toevoegen, selecteer Productie, geef deze de naam &quot;Productomgeving&quot; en selecteer de Akamai-adapter. Klik op Maken en vervolgens op Sluiten.

## Een ontwikkelbibliotheek maken

Ondanks alle tot dusver aangebrachte wijzigingen en configuraties is er geen code gepubliceerd. Als u een bibliotheek maakt die ruwweg is vertaald als een verzameling wijzigingen, kunt u code publiceren die op uw site wordt gebruikt.

1. Aanmelden bij de [UI voor gegevensverzameling](https://experience.adobe.com/data-collection) met uw Adobe-id-referenties.
2. Klik op de eigenschap tag die u op uw site wilt implementeren.
3. Klik op het tabblad Publiceren en klik vervolgens op Nieuwe bibliotheek toevoegen.
4. Geef de bibliotheek de naam &#39;Aanvankelijke wijzigingen&#39; en selecteer de ontwikkelomgeving.
5. Klik op Alle gewijzigde bronnen toevoegen. Hierin worden automatisch Adobe Analytics, Identity Service en Core vermeld.
6. Klik op Opslaan.
7. Klik op het scherm met de publicatieworkflow op het vervolgkeuzemenu naast de nieuwe bibliotheek en klik op Samenstellen voor ontwikkeling. Na een paar seconden wordt de gele stip in de bibliotheek groen om aan te geven dat het samenstellen is gelukt.
8. Ga naar het tabblad Milieu en klik vervolgens op de ontwikkelomgeving.
9. Kopieer de codeblokken onder &#39;Installatietags&#39; en geef deze door aan de eigenaars van de website van uw organisatie.

## Tags installeren in de ontwikkelomgeving van uw website

Als u de code van uw website beheert, implementeert u de twee codeblokken op de respectievelijke locaties (in het gedeelte `<head>` -tag en net boven het sluiten `</body>` -tag) op elke pagina van uw site. Deze code wordt algemeen geplaatst in het overkoepelende malplaatje van de plaats. Een lege pagina die alleen implementatiecode bevat, ziet er als volgt uit:

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

- [Snelstartgids](https://experienceleague.adobe.com/docs/experience-platform/tags/get-started/quick-start.html?lang=en): De basisworkflow van de implementatie van tags leren
- [Overzicht van publicatie](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/overview.html?lang=en): Meer informatie over publiceren en omgevingen

## Volgende stappen

[Uw analytische implementatie valideren en publiceren naar productie](validate-publish-prod.md): Begin waarde uit Adobe Analytics te halen.
