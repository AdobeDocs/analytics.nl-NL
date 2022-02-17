---
title: H Code JavaScript-implementatieoverzicht
description: Leer de workflow voor het implementeren van H-code op uw site.
feature: Implementation Basics
exl-id: cf83d8fe-a3b1-4e65-a86a-7eeaf555651b
source-git-commit: b3c74782ef6183fa63674b98e4c0fc39fc09441b
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 0%

---

# H Code JavaScript-implementatieoverzicht

>[!IMPORTANT]
>
>Deze versie van gegevensverzameling wordt niet meer ondersteund. Upgrade uitvoeren naar beide [tags in Adobe Experience Platform](../../launch/overview.md) of [AppMeasurement voor JavaScript](../overview.md).

U moet toegang hebben tot uw hostservers om een pagina met code te kunnen implementeren voor het verzamelen van gegevens. De volgende stappen lopen u door een basisimplementatie van de Code van Analytics H.

>[!NOTE]
>
>U moet al een bestaande kopie hebben van `s_code.js` om deze instructies te volgen. Adobe biedt niet langer een optie om H-code te downloaden in Codebeheer.

1. **Core JS-bestandsvariabelen bijwerken**: Bewerk de `s_code.js` en zorg ervoor dat de volgende variabelen worden bijgewerkt:
   * `s_account` bevat de rapportsuite-id waarnaar u gegevens wilt verzenden. Zie
   * `s.trackingServer` bevat de locatie waar cookies worden opgeslagen. Zie [trackingServer](../../vars/config-vars/trackingserver.md).
1. **De gastheer van `s_code.js` bestand op uw site**: Dit bestand bevindt zich gewoonlijk met andere scripts op uw webserver.
1. **Referentie `s_code.js` op alle pagina&#39;s**: Zorg ervoor dat alle afzonderlijke pagina&#39;s het kern-JavaScript-bestand aanroepen en doe dit binnen de HTML `<body>` -tag (niet de `<head>` -tag).

   >[!TIP]
   >
   >H Code vereist dat de `s_code.js` script wordt aangeroepen binnen de `<body>` tag. Dit verschilt van andere implementatiemethoden, waarbij voor het merendeel scriptverwijzingen moeten worden opgenomen in de `<head>` tag.
1. **Paginaspecifieke variabelen op elke pagina definiëren**: Voor elke pagina moeten afzonderlijke variabelen worden gedefinieerd, zoals paginanaam of eVars. Afzonderlijke variabelen worden doorgaans met een inline gedefinieerd `<script>` op elke pagina.
1. **Gebruik debugger om gegevensinzameling te verifiëren**: Download en installeer de [Experience Cloud debugger](../../validate/debugger.md) om ervoor te zorgen dat gegevens naar Adobe worden verzonden en dat paginariabelen correct zijn gedefinieerd.

## Caching

Het JavaScript-bestand wordt in de browser van de bezoeker in de cache geplaatst nadat het voor het eerst is geladen en wordt doorgaans niet meer dan één keer per sessie gedownload. Het bestand wordt niet op elke pagina gedownload, ook al wordt het door elke pagina op de site gebruikt. Op de meeste websites maken gebruikers een gemiddelde van meer dan een paar paginaweergaven per sessie. Het overbrengen van JavaScript dat meerdere keren in dit bestand wordt gebruikt, kan dus resulteren in minder algemene gedownloade gegevens.

## H-codecompressie

Als u zich zorgen maakt over de downloadgrootte van de `s_code.js` bestand, raadt Adobe aan het bestand te comprimeren `s_code.js` bestand met GZIP. GZIP wordt ondersteund door alle grote browsers en biedt betere prestaties dan JavaScript-compressie. Zie [Mod_deflate van Apache-module](https://httpd.apache.org/docs/current/mod/mod_deflate.html) in de Apache-documentatie.
