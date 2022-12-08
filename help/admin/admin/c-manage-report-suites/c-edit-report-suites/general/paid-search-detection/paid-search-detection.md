---
description: Met Betaalde zoekdetectie wordt onderscheid gemaakt tussen betalingen en natuurlijke zoekopdrachten in de rapporten Zoekprogramma's en Trefwoorden zoeken.
title: Detectie van betaalde zoekopdracht
feature: Admin Tools
exl-id: 6b513ad2-f955-4a34-92f8-57a141e44801
source-git-commit: 71ff81a0ae67c6f4cc9a8df567e27223cc63f18c
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# Detectie van betaalde zoekopdracht

[!UICONTROL Paid Search Detection] onderscheidt betaalde van natuurlijke zoekopdrachten in de [!UICONTROL Search Engines] en [!UICONTROL Search Keywords] rapporten. U kunt de zoekmachines opgeven waar u betaalde advertenties gebruikt en een tekenreeks opgeven die u kunt vinden in de URL van een bezoek van een betaalde advertentie.

## Configuratieopties {#section_0C2CFA0AF77B47098BE37CB024665D0D}

In de volgende tabel worden de velden en opties beschreven waarmee u [betaalbaar zoeken configureren](/help/admin/admin/c-manage-report-suites/c-edit-report-suites/general/paid-search-detection/t-paid-search-detection.md).

| Optie | Beschrijving |
| --- | --- |
| [!UICONTROL Search Engine] | Selecteer een zoekprogramma in de vervolgkeuzelijst. U geeft de engine op als u verschillende parameters voor de queryreeks gebruikt voor verschillende zoekprogramma&#39;s. Gewoonlijk wordt de waarde `Any` volstaat. |
| [!UICONTROL Query string] | Specificeert een koord voor een case-sensitive gelijke met om het even welk deel van de parameter van het vraagkoord, dat het deel van url na &quot;?&quot; is. <br>**Opmerking**: [!UICONTROL Paid Search Detection] is hoofdlettergevoelig. Een regel die bijvoorbeeld &quot;PID&quot; opgeeft als parameter voor een querytekenreeks, komt niet overeen met &quot;pid&quot;. Als uw organisatie gemengde gevallen gebruikt, plaats de nauwkeurige waarden als afzonderlijke regels, zodat kunnen alle gewenste parameters van het vraagkoord worden gevangen. |
