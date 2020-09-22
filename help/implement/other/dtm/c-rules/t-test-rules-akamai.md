---
description: Test niet-gepubliceerde regels vanaf uw console als u Akamai-hosting gebruikt.
keywords: Dynamic Tag Management;rule;switcher plug-in;akamai;test akamai;unpublished rules;test unpublished rules;debug rule
solution: Experience Cloud,Analytics,Target
title: Niet-gepubliceerde regels voor Akamai-hosting testen
uuid: 979e3d74-8d96-47d0-b581-cf5371248434
translation-type: tm+mt
source-git-commit: a4542164031fc9f181dfdc471a1d54b5056b1223
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 10%

---


# Niet-gepubliceerde regels voor Akamai-hosting testen

Test niet-gepubliceerde regels vanaf uw console als u Akamai-hosting gebruikt.

De insteekmodule van de Schakelaar is vaak de gemakkelijkste manier om te testen. Zie [Zoeken in insteekmodules](https://docs.adobe.com/content/help/en/dtm/using/resources/plugins/search-discovery-plugins.html) in de documentatie bij producten voor dynamisch tagbeheer voor meer informatie.

De volgende stappen tonen hoe te om te testen zonder de elektrisch toestel van de Schakelaar te gebruiken:

1. Open de webconsole op uw site en typ `localStorage.setItem('sdsat_stagingLibrary', true)`.
1. Druk op **[!UICONTROL Enter]**.
1. Typ `_satellite.setDebug(true)`en druk op **[!UICONTROL Enter]**.
1. Vernieuw de pagina.

   Deze actie laadt uw het opvoeren bibliotheek en plaatst debugger, zodat u details van alle beschikbare (gepubliceerde/unpublished) regels kunt zien die op de pagina vuren.
1. Als u klaar bent, voert u uit `localStorage.setItem('sdsat_stagingLibrary', false)`en drukt u op **[!UICONTROL Enter]**.

   Stap Resultaat
