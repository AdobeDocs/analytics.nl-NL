---
title: Problemen met H-code-implementaties oplossen
description: Leer enkele algemene problemen met verouderde JavaScript-implementaties.
exl-id: 51d6e286-7008-4736-a196-bd8ac4e3e9cb
source-git-commit: 562ed0e190954b7687fa79efaf5c5c54eb202af8
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# Problemen met H-code-implementaties oplossen

Hieronder vindt u stappen voor het oplossen van problemen die specifiek zijn voor H-code-implementaties.

## Analysecode in koptag plaatsen

>[!NOTE]
>
>Hoewel voor H-code-implementaties naar code moet worden verwezen in de `<body>`-tag, moet voor andere implementaties (zoals het gebruik van tags in Adobe Experience Platform) naar code worden verwezen in de `<head>`-tag.

Met de analysecode wordt een onzichtbare afbeelding van 1 x 1 pixel gemaakt. Eerder was het gebruikelijk om de `s_code.js` verwijzing in `<head>` markering te plaatsen. Door de code hier te plaatsen, kon de afbeelding de paginalay-out op geen enkele manier beïnvloeden. Het wordt ook sneller uitgevoerd, waardoor u paginaweergaven kunt tellen voor het gedeeltelijk laden van de pagina.

Bepaalde elementen van de code vereisen echter het bestaan van het object `<body>`. Als de JavaScript-code Analytics zich in de tag `<head>` bevindt, wordt deze uitgevoerd voordat het object `<body>` bestaat. Hierdoor worden in uw implementatie geen [!UICONTROL ClickMap]-gegevens verzameld, worden bestanden niet automatisch bijgehouden bij het downloaden of afsluiten van koppelingen, of gegevens van het verbindingstype. Het plaatsen van de manuscriptverwijzing naar `s_code.js` in de `<head>` markering werkt, maar het resultaat is een zeer beperkte versie van Analytics.

De analysecode kan overal binnen de `<body>` markering van een goed gevormde HTML- pagina worden geplaatst. Adobe raadt u aan de analytische code zo dicht mogelijk boven aan de tag `<body>` te plaatsen. Zorg ervoor dat paginariabelen worden ingesteld nadat het bestand `s_code.js` is geladen.

>[!TIP]
>
>Als u Adobe Analytics wilt integreren met Adobe Target, moet het include-bestand voor JavaScript onder aan de pagina worden geplaatst.
