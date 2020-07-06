---
title: Problemen met H-code-implementaties oplossen
description: Leer enkele algemene problemen met verouderde JavaScript-implementaties.
translation-type: tm+mt
source-git-commit: c4833525816d81175a3446215eb92310ee4021dd
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---


# Problemen met H-code-implementaties oplossen

Hieronder vindt u stappen voor het oplossen van problemen die specifiek zijn voor H-code-implementaties.

## Analytics-code in de koptag plaatsen

>[!NOTE]
>
>Terwijl de implementaties van de Code van H code vereist code in de `<body>` markering worden van verwijzingen voorzien, andere implementaties (zoals het gebruiken van de Lancering van het Adobe Experience Platform) vereisen code in de `<head>` markering wordt van verwijzingen voorzien.

Analytics-code maakt een onzichtbare afbeelding van 1 x 1 pixel. Eerder was het gebruikelijk om de `s_code.js` verwijzing in de `<head>` markering te plaatsen. Door de code hier te plaatsen, kon de afbeelding de paginalay-out op geen enkele manier beïnvloeden. Het wordt ook sneller uitgevoerd, waardoor u paginaweergaven kunt tellen voor het gedeeltelijk laden van de pagina.

Bepaalde elementen van de code vereisen echter het bestaan van het `<body>` object. Als de Analytics JavaScript-code in de `<head>` tag staat, wordt deze uitgevoerd voordat het `<body>` object bestaat. Hierdoor worden in uw implementatie geen [!UICONTROL ClickMap] gegevens verzameld, worden bestanden niet automatisch bijgehouden bij het downloaden of afsluiten van koppelingen, of worden gegevens van het verbindingstype niet geregistreerd. Het plaatsen van de scriptverwijzing naar `s_code.js` in de `<head>` markering werkt, maar het resultaat is een zeer beperkte versie van Analytics.

De Analytics-code kan overal in de `<body>` tag van een goed gevormde HTML-pagina worden geplaatst. Adobe raadt u aan de Analytics-code zo dicht mogelijk boven aan de `<body>` tag te plaatsen. Zorg ervoor dat paginariabelen worden ingesteld nadat het `s_code.js` bestand is geladen.

>[!TIP]
>
>Als u Adobe Analytics wilt integreren met Adobe Target, moet het include-bestand voor JavaScript onder aan de pagina worden geplaatst.
