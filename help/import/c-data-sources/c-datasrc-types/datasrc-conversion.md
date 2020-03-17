---
description: Gegevensbronnen ondersteunen de volgende dimensies en metriek van conversiegegevens voor gegevenstypen die als conversie worden verwerkt.
subtopic: Data sources
title: Conversie
topic: Developer and implementation
uuid: 5e7907b1-6c9c-4073-876b-410f3a29767d
translation-type: tm+mt
source-git-commit: ''

---


# Conversie

Gegevensbronnen ondersteunen de volgende dimensies en metriek van conversiegegevens voor gegevenstypen die als conversie worden verwerkt.

## Afmetingen en metingen van omzetting {#section_FA1731B232B246DABEDF5A5D84159084}

Als u een weergavegebeurtenis opgeeft, moet u ook de corresponderende gegevensdimensie (eVar) opgeven. Als u bijvoorbeeld Var2-weergaven opneemt, moet u Var2 met een waarde weergeven. Het aantal aangepaste gebeurtenissen en eVar-weergaven dat door een rapportsuite wordt ondersteund, is afhankelijk van het contract en verschilt per bedrijf.

<p class="head"> <b>Omzetafmetingen</b> </p>

| Kolomnaam | Beschrijving |
|--- |--- |
| Trackingcode | Naam van trackingcode. |
| Datum | Gebruik de volgende datumnotatie:  MM/DD/YYYY/HH/mm/SS (bijvoorbeeld 01/01/2015/06/00/00) |
| Categorie | Naam categorie.  Als u een categorie opgeeft, moet u ook een product selecteren. |
| Kanaal | Kanaalnaam. |
| Varn | Varkensnaam. Geldige waarden voor n zijn geheel getal 1 - 75. |
| Product | Productnaam. |
| Staat | Framenaam. |
| Postcode | Postnaam. |

<p class="head"> <b>Conversiedetecties</b> </p>

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
