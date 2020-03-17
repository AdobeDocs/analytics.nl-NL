---
description: Controleer of uw Dynamic Tag Management-bibliotheek correct op uw site wordt geladen.
keywords: Analytics Implementation;implementation method;dynamic tag management;dtm;code;page code;header code;footer code;embed code;verify code;verify header code;verify footer code;embed tab;embed
title: Koptekst- en voettekstcode controleren
topic: Developer and implementation
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
translation-type: tm+mt
source-git-commit: ebf149df7974f9f2889b6fe938088eda90c84051

---


# Koptekst- en voettekstcode controleren

Controleer of uw Dynamic Tag Management-bibliotheek correct op uw site wordt geladen.

1. Open uw site in uw browser.
1. Open het venster [!UICONTROL Developer Console] door met de rechtermuisknop te klikken en **[!UICONTROL Inspect Element]** > **[!UICONTROL Console]** te kiezen.
1. Druk op **[!UICONTROL Enter]**.

   Als de code correct geïnstalleerd was, zult u *`true`* vertoning in de console zien.

   Als de code niet correct is geïnstalleerd, wordt de referentiefout weergegeven:

   `_satellite is not defined`

   Als deze fout optreedt, controleert u of:

* U hebt de volledige koptekstcode op elke pagina van de site opgenomen in de [!DNL HEAD] sectie, net als in de [!DNL <head><meta http-equiv="Content-Type" content="text/html; charset=UTF-8">] -tag indien mogelijk.
* Er verschijnen geen onverwachte tekens in het codefragment, mogelijk als gevolg van kopiëren en plakken vanuit een opgemaakt document.

