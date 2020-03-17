---
title: H Code JavaScript-implementatieoverzicht
description: Leer de workflow voor het implementeren van H-code op uw site.
translation-type: tm+mt
source-git-commit: 664d0cde8b8b17c86b47858611d459026aab0bef

---


# H Code JavaScript-implementatieoverzicht

> [!IMPORTANT] Deze versie van gegevensverzameling wordt niet meer ondersteund. Voer een upgrade uit naar [Adobe Experience Platform Launch](../../launch/overview.md) of [AppMeasurement voor JavaScript](../overview.md).

U moet toegang hebben tot uw hostservers om een pagina met code te kunnen implementeren voor het verzamelen van gegevens. De volgende stappen lopen u door een basisimplementatie van de Code van Analytics H.

> [!NOTE] U moet al over een bestaand exemplaar van beschikken om deze instructies `s_code.js` te kunnen volgen. Adobe biedt niet langer een optie om H-code te downloaden in Codebeheer.

1. **Core JS-bestandsvariabelen** bijwerken: Bewerk het `s_code.js` bestand en controleer of de volgende variabelen zijn bijgewerkt:
   * `s_account` bevat de rapportsuite-id waarnaar u gegevens wilt verzenden. Zie
   * `s.trackingServer` bevat de locatie waar cookies worden opgeslagen. Zie [trackingServer](../../vars/config-vars/trackingserver.md).
2. **Het`s_code.js`bestand hosten op uw site**: Dit bestand bevindt zich gewoonlijk met andere scripts op uw webserver.
3. **Referentie`s_code.js`op alle pagina**&#39;s: Zorg ervoor dat alle afzonderlijke pagina&#39;s het kern-JavaScript-bestand aanroepen en doe dit binnen de HTML- `<body>` tag (niet de `<head>` -tag).
   > [!TIP] H Code vereist dat het `s_code.js` script binnen de `<body>` tag wordt aangeroepen. Dit verschilt van andere implementatiemethoden, waarbij voor de meeste van deze methoden scriptverwijzingen in de `<head>` tag moeten staan.
4. **Definieer paginaspecifieke variabelen op elke pagina**: Voor elke pagina moeten afzonderlijke variabelen worden gedefinieerd, zoals paginanaam of eVars. Afzonderlijke variabelen worden doorgaans op elke pagina gedefinieerd met een inline- `<script>` tag.
5. **Gebruik debugger om gegevensinzameling** te verifiëren: Download en installeer het foutopsporingsprogramma [voor de](../../validate/debugger.md) Experience Cloud om te controleren of gegevens naar Adobe worden verzonden en of de paginabariabelen correct zijn gedefinieerd.

## Caching

Het JavaScript-bestand wordt in de browser van de bezoeker in de cache geplaatst nadat het voor het eerst is geladen en wordt doorgaans niet meer dan één keer per sessie gedownload. Het bestand wordt niet op elke pagina gedownload, ook al wordt het door elke pagina op de site gebruikt. Op de meeste websites maken gebruikers een gemiddelde van meer dan een paar paginaweergaven per sessie. Het overbrengen van JavaScript dat meerdere keren in dit bestand wordt gebruikt, kan dus resulteren in minder algemene gedownloade gegevens.

## H-codecompressie

Als u zich zorgen maakt over de downloadgrootte van het `s_code.js` bestand, raadt Adobe aan het `s_code.js` bestand te comprimeren met GZIP. GZIP wordt ondersteund door alle grote browsers en biedt betere prestaties dan JavaScript-compressie. Zie Mod_deflate [van](http://httpd.apache.org/docs/current/mod/mod_deflate.html) Apache Module in de documentatie van Apache.
