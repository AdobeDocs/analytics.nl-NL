---
title: H-code-implementaties oplossen
description: Leer enkele algemene problemen met oudere JavaScript-implementaties.
feature: Implementation Basics
exl-id: 51d6e286-7008-4736-a196-bd8ac4e3e9cb
role: Developer
source-git-commit: 7d8df7173b3a78bcb506cc894e2b3deda003e696
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---

# H-code-implementaties oplossen

Hieronder vindt u stappen voor het oplossen van problemen die specifiek zijn voor H-code-implementaties.

## Analysecode in koptag plaatsen

>[!NOTE]
>
>Hoewel voor H-code-implementaties naar code moet worden verwezen in het dialoogvenster `<body>` -tag, andere implementaties (zoals het gebruik van tags in Adobe Experience Platform) vereisen dat naar code wordt verwezen in de `<head>` -tag.

Met de analysecode wordt een onzichtbare afbeelding van 1 x 1 pixel gemaakt. Voorheen was het een gangbare praktijk om de `s_code.js` in de `<head>` -tag. Door de code hier te plaatsen, kon de afbeelding de paginalay-out op geen enkele manier beïnvloeden. Het wordt ook sneller uitgevoerd, waardoor u paginaweergaven kunt tellen voor het gedeeltelijk laden van de pagina.

Bepaalde elementen van de code vereisen echter het bestaan van `<body>` object. Als de JavaScript-code Analytics voorkomt in het dialoogvenster `<head>` -tag, wordt deze uitgevoerd vóór de `<body>` object bestaat. Hierdoor wordt uw implementatie niet verzameld [!UICONTROL ClickMap] gegevens, het automatisch volgen van dossierdownloads of uitgangsverbindingen, of verbindingstype gegevens. De scriptverwijzing plaatsen naar `s_code.js` in de `<head>` -tag werkt, maar het resultaat is een zeer beperkte versie van Analytics.

De analysecode kan overal binnen `<body>` -tag van een goed gevormde HTML-pagina. Adobe raadt u aan de analytische code zo dicht mogelijk bij de bovenkant van de `<body>` -tag indien mogelijk. Zorg ervoor dat alle paginariabelen zijn ingesteld na het dialoogvenster `s_code.js` bestand wordt geladen.

>[!TIP]
>
>Als u Adobe Analytics wilt integreren met Adobe Target, moet het include-bestand voor JavaScript onder aan de pagina worden geplaatst.
