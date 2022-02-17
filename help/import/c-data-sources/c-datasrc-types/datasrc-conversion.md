---
description: Gegevensbronnen ondersteunen de volgende dimensies en metriek van conversiegegevens voor gegevenstypen die als conversie worden verwerkt.
subtopic: Data sources
title: Conversie
topic-fix: Developer and implementation
feature: Data Sources
exl-id: 00450ad4-7148-4cf1-bdba-5d1732dd0fd3
source-git-commit: 79294cfc6f86e5a41a39504099cd730f53668725
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 5%

---

# Conversie

Gegevensbronnen ondersteunen de volgende dimensies en metriek van conversiegegevens voor gegevenstypen die als conversie worden verwerkt.

## Dimension voor conversie en metriek {#section_FA1731B232B246DABEDF5A5D84159084}

Als u een weergavegebeurtenis opgeeft, moet u ook de corresponderende gegevensdimensie (eVar) opgeven. Als u bijvoorbeeld eVar2-weergaven opneemt, moet u een waarde opgeven voor eVar2. Het aantal aangepaste gebeurtenissen en weergaven die door een rapportsuite worden ondersteund, is afhankelijk van het contract en verschilt per bedrijf.

<p class="head"> <b>Conversiedimensies</b> </p>

| Kolomnaam | Beschrijving |
|--- |--- |
| Trackingcode | Naam van trackingcode. |
| Datum | Gebruik de volgende datumnotatie: MM/DD/YYYY/HH/mm/SS (bijvoorbeeld 01/01/2015/06/00/00) |
| Categorie | Naam categorie.  Als u een categorie opgeeft, moet u ook een product selecteren. |
| Kanaal | Kanaalnaam. |
| Varn | Varkensnaam. Geldige waarden voor n zijn geheel getal 1 - 250. |
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
| Weergaven winkelwagen | Aantal winkelwagentjes. |
| Betalingen | Aantal kassa&#39;s. |
| Gebeurtenis n | Aantal keren dat gebeurtenis n heeft plaatsgevonden. Geldige waarden voor n zijn geheel getal 1 - 100.  Als u een weergavegebeurtenis opgeeft, moet u ook de corresponderende gegevensdimensie (eVar) opgeven. Als u bijvoorbeeld eVar2-weergaven opneemt, moet u een waarde opgeven voor eVar2. |
| Diverse weergaven | Aantal malen dat eVar n is weergegeven. Geldige waarden voor n zijn geheel getal 1 - 250. |
| Prijs | Productprijs. |
| Orders | Aantal geplaatste bestellingen. |
| Productweergaven | Aantal productweergaven. |
| Aantal | Aantal verkochte eenheden. |
