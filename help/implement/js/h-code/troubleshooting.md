---
title: Problemen met H-code-implementaties oplossen
description: Leer enkele algemene problemen met verouderde JavaScript-implementaties.
translation-type: tm+mt
source-git-commit: 69138bdedb42b66449426fee39822520ee4b1198

---


# Problemen met H-code-implementaties oplossen

Hieronder vindt u stappen voor het oplossen van problemen die specifiek zijn voor H-code-implementaties.

## Analysecode in koptag plaatsen

> [!NOTE] Hoewel voor H Code-implementaties in de `<body>` tag naar code moet worden verwezen, moet voor andere implementaties (zoals het gebruik van Adobe Experience Platform Launch) naar code worden verwezen in de `<head>` tag.

Met de analysecode wordt een onzichtbare afbeelding van 1 x 1 pixel gemaakt. Eerder was het gebruikelijk om de `s_code.js` verwijzing in de `<head>` markering te plaatsen. Door de code hier te plaatsen, kon de afbeelding de paginalay-out op geen enkele manier beïnvloeden. Het wordt ook sneller uitgevoerd, waardoor u paginaweergaven kunt tellen voor het gedeeltelijk laden van de pagina.

Bepaalde elementen van de code vereisen echter het bestaan van het `<body>` object. Als de JavaScript-code Analytics in de `<head>` tag staat, wordt deze uitgevoerd voordat het `<body>` object bestaat. Hierdoor worden in uw implementatie geen [!UICONTROL ClickMap] gegevens verzameld, worden bestanden niet automatisch bijgehouden bij het downloaden of afsluiten van koppelingen, of worden gegevens van het verbindingstype niet geregistreerd. Het plaatsen van de manuscriptverwijzing naar `s_code.js` in de `<head>` markering werkt, maar het resultaat is een zeer beperkte versie van Analytics.

De analysecode kan overal binnen de markering van een goed gevormde HTML- pagina worden geplaatst. `<body>` Adobe raadt u aan de analytische code zo dicht mogelijk boven aan de `<body>` tag te plaatsen. Zorg ervoor dat paginariabelen worden ingesteld nadat het `s_code.js` bestand is geladen.

> [!TIP] Als u Adobe Analytics wilt integreren met Adobe Target, moet het include-bestand voor JavaScript onder aan de pagina worden geplaatst.
