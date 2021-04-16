---
description: Controleer of uw Dynamic Tag Management-bibliotheek correct op uw site wordt geladen.
keywords: Analyse-implementatie;implementatiemethode;dynamisch tagbeheer;dtm;code;paginacode;koptekstcode;voettekstcode;insluitcode;controleer de koptekstcode;controleer de voettekstcode;controleer de voettekstcode;sluit het tabblad in;embed
title: Code voor kop- en voetteksten controleren
topic-fix: Developer and implementation
uuid: d395a417-0c61-41a6-a124-d2f400f4626f
exl-id: bed44ba7-8e0e-49e2-bedc-fb1ba66e5b18
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 6%

---

# Code voor kop- en voetteksten controleren

Controleer of uw Dynamic Tag Management-bibliotheek correct op uw site wordt geladen.

1. Open uw site in uw browser.
1. Open [!UICONTROL Developer Console] door met de rechtermuisknop te klikken en **[!UICONTROL Inspect Element]** > **[!UICONTROL Console]** te kiezen.
1. Druk op **[!UICONTROL Enter]**.

   Als de code correct geïnstalleerd was, zult u *`true`* vertoning in de console zien.

   Als de code niet correct is geïnstalleerd, wordt de referentiefout weergegeven:

   `_satellite is not defined`

   Als deze fout optreedt, controleert u of:

* U hebt de volledige koptekstcode op elke pagina van de site opgenomen in de sectie [!DNL HEAD], zo dicht mogelijk bij de tag `<head>`.
* Er verschijnen geen onverwachte tekens in het codefragment, mogelijk als gevolg van kopiëren en plakken vanuit een opgemaakt document.
