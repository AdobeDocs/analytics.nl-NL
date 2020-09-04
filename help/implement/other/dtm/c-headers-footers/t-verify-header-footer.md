---
description: Controleer of uw Dynamic Tag Management-bibliotheek correct op uw site wordt geladen.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;code;page code;header code;footer code;embed code;verify code;verify header code;verify footer code;embed tab;embed
title: Code voor kop- en voetteksten controleren
topic: Developer and implementation
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
translation-type: tm+mt
source-git-commit: 82cf5ddfd4d18af09c2dbedba20514e4b643a94b
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 7%

---


# Code voor kop- en voetteksten controleren

Controleer of uw Dynamic Tag Management-bibliotheek correct op uw site wordt geladen.

1. Open uw site in uw browser.
1. Open het venster [!UICONTROL Developer Console] door met de rechtermuisknop te klikken en **[!UICONTROL Inspect Element]** > **[!UICONTROL Console]** te kiezen.
1. Druk op **[!UICONTROL Enter]**.

   Als de code correct geïnstalleerd was, zult u *`true`* vertoning in de console zien.

   Als de code niet correct is geïnstalleerd, wordt de referentiefout weergegeven:

   `_satellite is not defined`

   Als deze fout optreedt, controleert u of:

* U hebt de volledige koptekstcode op elke pagina van de site opgenomen in de [!DNL HEAD] sectie, zo dicht mogelijk bij de `<head>` tag.
* Er verschijnen geen onverwachte tekens in het codefragment, mogelijk als gevolg van kopiëren en plakken vanuit een opgemaakt document.

