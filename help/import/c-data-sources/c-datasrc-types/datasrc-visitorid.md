---
description: Bezoeker-id's kunnen worden geïntegreerd door de categorie Algemeen (Transactie-id) te selecteren.
subtopic: Data sources
title: Bezoeker-id
topic: Developer and implementation
uuid: 4e9ce675-72c2-42a4-8f2e-25140df19539
translation-type: tm+mt
source-git-commit: 99ee24efaa517e8da700c67818c111c4aa90dc02

---


# Bezoeker-id

Bezoeker-id&#39;s kunnen worden geïntegreerd door de categorie Algemeen (Transactie-id) te selecteren.

Zie Offlinegegevens [integreren](/help/import/c-data-sources/datasrc-integrating-offline-data.md).

<p class="head"> <b>Afmetingen bezoeker-id</b> </p>

| Kolomnaam | Beschrijving |
|--- |--- |
| Bezoeker-id | (Vereist) Unieke waarde die een klant in zowel de online als de off-line systemen vertegenwoordigt. |
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
| Kleuraweergaven | Aantal winkelwagentjes. |
| Afbeeldingen | Aantal kassa&#39;s. |
| Gebeurtenis n | Aantal keren dat gebeurtenis n heeft plaatsgevonden. Geldige waarden voor n zijn geheel getal 1 - 100.  Als u een weergavegebeurtenis opgeeft, moet u ook de corresponderende gegevensdimensie (eVar) opgeven. Als u bijvoorbeeld Var2-weergaven opneemt, moet u Var2 met een waarde weergeven. |
| Diverse weergaven | Aantal malen dat eVar n is weergegeven. Geldige waarden voor n zijn geheel getal 1 - 75. |
| Prijs | Productprijs. |
| Orders | Aantal geplaatste bestellingen. |
| Productweergaven | Aantal productweergaven. |
| Aantal | Aantal verkochte eenheden. |
