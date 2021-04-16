---
description: Bezoeker-id's kunnen worden geïntegreerd door de categorie Algemeen (Transactie-id) te selecteren.
subtopic: Data sources
title: Bezoekers-id
topic-fix: Developer and implementation
uuid: 4e9ce675-72c2-42a4-8f2e-25140df19539
exl-id: 940af1ba-0d12-4552-a21e-0ceb06427ab2
translation-type: tm+mt
source-git-commit: 78412c2588b07f47981ac0d953893db6b9e1d3c2
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 7%

---

# Bezoekers-id

Bezoeker-id&#39;s kunnen worden geïntegreerd door de categorie Algemeen (Transactie-id) te selecteren.

Zie [Offlinegegevens integreren](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

<p class="head"> <b>Dimension van bezoeker-id</b> </p>

| Kolomnaam | Beschrijving |
|--- |--- |
| Bezoekers-id | (Vereist) Unieke waarde die een klant in zowel de online als de off-line systemen vertegenwoordigt. |
| Datum | Gebruik de volgende datumnotatie:  DD-MM-JJJJ/uu/mm/ss (bijvoorbeeld 07-14-2017-06-00/00) |
| Trackingcode | Naam van trackingcode. |
| Categorie | Naam categorie.  Als u een categorie opgeeft, moet u ook een product selecteren. |
| Kanaal | Kanaalnaam. |
| Varn | Varkensnaam. Geldige waarden voor n zijn geheel getal 1 - 75. |
| Product | Productnaam. |
| Staat | Framenaam. |
| Postcode | Postnaam. |

**Metrische gegevens van bezoeker-id**

| Kolomnaam | Beschrijving |
|--- |--- |
| Klikdoorhalingen | Aantal weergaven van code bijhouden. |
| Extra winkelwagentjes | Aantal toevoegingen aan winkelwagentjes. |
| Kleurafopen | Aantal winkelwagentjes. |
| Winkelwagentjes verwijderen | Aantal winkelwagentjes. |
| Weergaven winkelwagen | Aantal winkelwagentjes. |
| Betalingen | Aantal kassa&#39;s. |
| Gebeurtenis n | Aantal keren dat gebeurtenis n heeft plaatsgevonden. Geldige waarden voor n zijn geheel getal 1 - 100.  Als u een weergavegebeurtenis opgeeft, moet u ook de corresponderende gegevensdimensie (eVar) opgeven. Als u bijvoorbeeld eVar2-weergaven opneemt, moet u een waarde opgeven voor eVar2. |
| Diverse weergaven | Aantal malen dat eVar n is weergegeven. Geldige waarden voor n zijn geheel getal 1 - 75. |
| Prijs | Productprijs. |
| Orders | Aantal geplaatste bestellingen. |
| Productweergaven | Aantal productweergaven. |
| Aantal | Aantal verkochte eenheden. |
