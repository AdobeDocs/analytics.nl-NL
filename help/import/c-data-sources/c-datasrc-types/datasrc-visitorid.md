---
description: Bezoeker-id's kunnen worden geïntegreerd door de categorie Algemeen (Transactie-id) te selecteren.
subtopic: Data sources
title: Bezoekers-id
topic-fix: Developer and implementation
uuid: 4e9ce675-72c2-42a4-8f2e-25140df19539
exl-id: 940af1ba-0d12-4552-a21e-0ceb06427ab2
source-git-commit: a7a116ddc9eddc500a52111e9c002bdbee3e4a56
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 2%

---

# VisitorID

Bezoeker-id&#39;s kunnen worden geïntegreerd door de optie [!UICONTROL Call Center Data] categorie.

Zie [Offline gegevens integreren](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

## Dimension van VisitorID

| Kolomnaam | Beschrijving |
|--- |--- |
| [!UICONTROL VisitorID] | (Vereist) Unieke waarde die een klant in zowel de online als de off-line systemen vertegenwoordigt. |
| [!UICONTROL Date] | Gebruik de volgende datumnotatie: `MM/DD/YYYY/hh/mm/ss` (bijvoorbeeld 07/14/2017/06/00/00) |
| [!UICONTROL Tracking Code] | Naam van trackingcode. |
| [!UICONTROL Category] | Naam categorie. Als u een categorie opgeeft, moet u ook een product selecteren. |
| [!UICONTROL Channel] | Kanaalnaam. |
| [!UICONTROL eVar]*n* | eVar *n* naam. Geldige waarden voor *n* zijn de gehele getallen 1 - 75. |
| [!UICONTROL Product] | Productnaam. |
| [!UICONTROL State] | Framenaam. |
| [!UICONTROL Zip] | Postnaam. |

## Metrische gegevens van bezoeker-id

| Kolomnaam | Beschrijving |
| --- | --- |
| [!UICONTROL Clickthroughs] | Aantal weergaven van code bijhouden. |
| [!UICONTROL Cart Adds] | Aantal toevoegingen aan winkelwagentjes. |
| [!UICONTROL Cart Opens] | Aantal winkelwagentjes. |
| [!UICONTROL Cart Removes] | Aantal winkelwagentjes. |
| [!UICONTROL Cart Views] | Aantal winkelwagentjes. |
| [!UICONTROL Checkouts] | Aantal kassa&#39;s. |
| [!UICONTROL Event]*n* | Aantal even keren *n* is opgetreden. Geldige waarden voor n zijn geheel getal 1 - 100.  Als u een [!UICONTROL View] -gebeurtenis, moet u ook de corresponderende gegevensdimensie (eVar) opgeven. Als u bijvoorbeeld eVar2-weergaven opneemt, moet u een waarde opgeven voor eVar2. |
| [!UICONTROL eVar]*n* Weergaven | Aantal keren eVar *n* is bekeken. Geldige waarden voor *n* zijn de gehele getallen 1 - 75. |
| [!UICONTROL Price] | Productprijs. |
| [!UICONTROL Orders] | Aantal geplaatste bestellingen. |
| [!UICONTROL Product Views] | Aantal productweergaven. |
| [!UICONTROL Quantity] | Aantal verkochte eenheden. |
