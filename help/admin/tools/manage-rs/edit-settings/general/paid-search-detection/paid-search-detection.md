---
description: Met Betaalde zoekdetectie wordt onderscheid gemaakt tussen betalingen en natuurlijke zoekopdrachten in de rapporten Zoekprogramma's en Trefwoorden zoeken.
title: Detectie van betaalde zoekopdracht
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
source-git-commit: a6967c7d4e1dca5491f13beccaa797167b503d6e
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# Detectie van betaalde zoekopdracht

In [!UICONTROL Paid Search Detection] wordt onderscheid gemaakt tussen betalingen en natuurlijke zoekopdrachten in de rapporten [!UICONTROL Search Engines] en [!UICONTROL Search Keywords] . U kunt de zoekmachines opgeven waar u betaalde advertenties gebruikt en een tekenreeks opgeven die u kunt vinden in de URL van een bezoek van een betaalde advertentie.

## Configuratieopties {#configuration}

De volgende lijst beschrijft de gebieden en de opties u gebruikt om [ betaalde onderzoeksopsporing ](/help/admin/tools/manage-rs/edit-settings/general/paid-search-detection/t-paid-search-detection.md) te vormen.

| Optie | Beschrijving |
| --- | --- |
| [!UICONTROL Search Engine] | Selecteer een zoekprogramma in de vervolgkeuzelijst. U geeft de engine op als u verschillende parameters voor de queryreeks gebruikt voor verschillende zoekprogramma&#39;s. Gewoonlijk is de waarde `Any` voldoende. |
| [!UICONTROL Query string] | Specificeert een koord voor een case-sensitive gelijke met om het even welk deel van de parameter van het vraagkoord, dat het deel van url na &quot;?&quot; is. <br>**Nota**: [!UICONTROL Paid Search Detection] is gevoelig geval. Een regel die bijvoorbeeld &quot;PID&quot; opgeeft als parameter voor een querytekenreeks, komt niet overeen met &quot;pid&quot;. Als uw organisatie gemengde gevallen gebruikt, plaats de nauwkeurige waarden als afzonderlijke regels, zodat kunnen alle gewenste parameters van het vraagkoord worden gevangen. |
